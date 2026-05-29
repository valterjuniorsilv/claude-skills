---
name: bom-dia
description: Retoma de onde Valter parou. Lê o estado salvo pelo último /boa-noite e apresenta resumo das pendências, próximas ações e bloqueios de cada sessão. Use quando Valter disser "/bom-dia", "bom dia", "o que tava pendente", "do que ficou", "retoma onde parei", "o que eu tava fazendo ontem". Pareado com /boa-noite.
---

# /bom-dia — Retomar Pendências

## Objetivo

Quando Valter abre o terminal de manhã, esse skill lê o estado salvo pelo último `/boa-noite` e mostra:
- O que ficou pendente em cada sessão
- Próximas ações priorizadas
- Bloqueios que precisam ser resolvidos
- Decisões que ainda não foram tomadas

Pressuposto: Valter rodou `/boa-noite` antes de dormir. Se não rodou, esse skill avisa que não tem estado salvo e oferece alternativa (analisar JSONLs recentes ad-hoc).

## Onde lê

- **Arquivo principal:** `~/.claude/state/last-night.json` (mais recente)
- **Histórico:** `~/.claude/state/last-night.YYYY-MM-DD.json` (cópias datadas, se Valter pedir "como foi quinta-feira")

## Algoritmo

### 1. Verificar se há estado salvo

```bash
test -f /Users/valtersilva/.claude/state/last-night.json && echo "EXISTS" || echo "MISSING"
```

Se MISSING:
- Avisar Valter
- Oferecer: "Quer que eu analise os JSONLs das últimas 24h direto pra montar o resumo? Vai gastar tokens mas funciona."
- Se sim: rodar lógica do `/boa-noite` em modo readonly (não salva vault, só extrai pendências)

### 2. Ler estado salvo

```bash
cat /Users/valtersilva/.claude/state/last-night.json | jq .
```

### 3. Apresentar resumo formatado

Formato:

```
=== BOM DIA, VALTER ===
Último /boa-noite: 28/04 01:00 (8h atrás)
Sessões salvas: 3

────────────────────────────────────────
[1] Workspace | NodusHub
────────────────────────────────────────
Última msg: "Vamos manter a idéia do warmup..."

Tasks abertas (3):
  • Re-disparar Wave Brasil (in_progress, scrape rodando)
  • Workflow N8N WhatsApp (em construção)
  • Workflow warmup com 8-9 inboxes (aguardando senha de app)

Próximas ações:
  → Validar DNS olympusodonto.com.br (deve ter propagado)
  → Rodar mail-tester.com pra verificar score
  → Gerar senha de app do 1º gmail pra warmup
  → Gravar criativo ads R$33/dia (deadline quarta)

Bloqueios:
  ⚠ Iris não testada com volume real (validar antes de ligar ads)

Decisões pendentes:
  ? Sistema de indicação formal (criar mês 2?)
  ? UI prospec botão "Ligar" antes de segunda?

────────────────────────────────────────
[2] Brenda
────────────────────────────────────────
[...repete...]

────────────────────────────────────────
PRIORIDADE DO DIA (sugestão)
────────────────────────────────────────
1. Validar DNS Olympus + mail-tester (5min, libera workflow)
2. Gerar senha de app gmail (5min, destrava warmup)
3. Gravar criativo ads (1-2h, deadline quarta)

Quer começar por qual?
```

### 4. Sugerir prioridade do dia

Heurística pra rankear:
1. **Bloqueio com TTL curto** (DNS propagando, scrape rodando) → mais alto
2. **Tarefa que destrava outras** (gerar senha → workflow warmup → cold email)
3. **Deadline próximo** (criativo ads quarta)
4. **Decisão pendente** (não bloqueia nada → mais baixo)

### 5. Não rodar tarefas automaticamente

`/bom-dia` é READ-ONLY. Mostra estado, sugere ordem, espera Valter escolher. Não dispara nada sozinho.

## Flags opcionais

- `/bom-dia full` — mostra TODAS as sessões com detalhe completo (default é resumo)
- `/bom-dia [projeto]` — só uma sessão específica (ex: `/bom-dia Workspace`)
- `/bom-dia historico` — lista últimas N noites salvas
- `/bom-dia ontem` — pega last-night.json mais recente independente da data

## Edge cases

### Estado salvo mas com mais de 48h

Avisar: "Último /boa-noite foi há 3 dias. Pode ter evoluído desde lá. Quer só ver o que tinha ou prefere ignorar e analisar JSONLs recentes?"

### Múltiplos arquivos last-night.YYYY-MM-DD.json

Se Valter rodou /boa-noite múltiplas vezes em dias diferentes, manter histórico mas usar SEMPRE o mais recente como default.

### Estado corrompido / JSON inválido

Avisar e oferecer modo manual: "JSON corrompido. Quer que eu reconstrua analisando os JSONLs das últimas 24h?"

### Sem estado e sem JSONLs recentes

Resposta direta: "Não tem nada salvo nem sessão recente. Provavelmente você teve fim de semana off. Bom dia limpo. O que vamos fazer hoje?"

## Conexão com outros skills

- **Pareado com `/boa-noite`** — sem boa-noite anterior, /bom-dia tem que cair em modo manual
- **Não substitui:** `/load-context` (que recupera contexto APÓS auto-compact, é diferente)
- **Complementa:** invocar `/save-vault` ao final do dia + `/boa-noite` antes de dormir = ciclo limpo

## Filosofia

`/boa-noite` salva o que importa pra retomar.
`/bom-dia` mostra de onde retomar.
Juntos: nenhum trabalho perdido entre os dias.
