---
name: boa-noite
description: Salva no Obsidian Vault o conteúdo relevante de TODAS as sessões Claude Code abertas (não só a atual). Use quando o Valter disser "/boa-noite", "vou dormir", "encerra tudo", "salva tudo dos terminais", "fechar o dia". Lê os JSONL das outras sessões direto do filesystem e processa cada uma como se fosse /save-vault. Ideal pra encerrar o dia com vários terminais abertos.
---

# /boa-noite — Salvar Vault Multi-Sessão

## Objetivo

Quando Valter encerra o dia com várias sessões Claude Code abertas, esse skill garante que conhecimento de TODAS é preservado no Obsidian Vault. Não só a sessão atual — todas que foram modificadas recentemente.

Pressuposto: ao rodar `/boa-noite`, Valter está fechando os terminais. Isso justifica processar as conversas como histórico.

---

## Limitações reais (avisar Valter no início)

1. **Cada terminal Claude Code é processo isolado** — não dá pra "executar /save-vault em outra sessão". O que esse skill faz é **ler os JSONL das outras sessões diretamente do filesystem** e processar cada um.

2. **Custo de tokens é alto** — processar 4-6 conversas longas consome muito contexto. É um custo aceitável pra encerrar o dia, não pra rodar várias vezes.

3. **Sessão sendo modificada DEPOIS de rodar /boa-noite** — se Valter continuar conversando em outro terminal depois desse skill processar, o que vier depois NÃO será salvo. Skill lê snapshot do JSONL no momento da execução.

4. **Skill processa TODAS as sessões ativas (modificadas nas últimas 24h)** — incluindo a atual.

---

## Algoritmo

### 1. Identificar sessões ativas

Listar arquivos `.jsonl` em `/Users/valtersilva/.claude/projects/*/` modificados nas últimas 24h:

```bash
find /Users/valtersilva/.claude/projects -name "*.jsonl" -mtime -1 -not -path "*/conversations/*" 2>/dev/null
```

Filtrar pra pegar apenas o JSONL mais recente por projeto (cada projeto pode ter várias sessões antigas, mas a mais recente é a "ativa").

### 2. Pra cada sessão ativa

Para cada `.jsonl` encontrado:

a. **Identificar projeto** — extrair do path (`-Users-valtersilva-X` → projeto X)
b. **Ler o conteúdo** — JSONL com mensagens user/assistant/tool
c. **Minerar conhecimento** — aplicar mesmos critérios do `/save-vault`:
   - Bugs com causa raiz
   - Decisões técnicas com trade-offs
   - Configurações/env vars descobertas
   - Padrões de código estabelecidos
   - URLs/endpoints ativos
   - Copy/tom aprovado
d. **Salvar no vault** — em `/Users/valtersilva/Documents/Obsidian Vault/`
   - Atualizar arquivos existentes (Glob antes)
   - Criar novos quando faz sentido
   - Frontmatter com `updated: hoje`
e. **Reportar** — formato resumido por sessão

### 3. Output formato

```
=== /boa-noite — Multi-Vault ===
Sessões processadas: N

[1] Workspace | NodusHub
    Última atividade: 27/04 18h
    Salvo: Projetos/Email-Cold-Olympus.md (atualizado)
           Conceitos/Email-Warmup-DIY.md (novo)
    Não salvo: nada relevante novo

[2] Brenda
    Última atividade: 26/04 22h
    Salvo: Projetos/Studio-Renova.md (atualizado)
    Não salvo: pequenos ajustes de copy (ja registrados)

[3] Apresentação de vendas - HP
    Última atividade: 27/04 11h
    Salvo: Comercial/Apresentacao-Vendas-HP.md (novo)

==========================================
Total: 3 arquivos atualizados, 2 novos
Tokens consumidos estimados: ~XXk
==========================================

Boa noite, Valter.
```

---

## Implementação passo a passo (Claude executa)

1. **Avisar limitações** — sempre que invocado, primeira coisa é mostrar 4 ressalvas (acima)
2. **Pedir confirmação** — "Vou processar N sessões, tokens estimados ~Xk. Confirma?" (esperar OK)
3. **Listar sessões** — bash find acima, agrupar por projeto
4. **Processar uma a uma** — abrir JSONL, mining, save no vault
5. **Output final** — resumo formatado

### Como ler o JSONL

```bash
# Cada linha é JSON com:
# - message.role: user|assistant|tool_use|tool_result
# - message.content: array de blocos
# - timestamp

# Pega só user+assistant (ignora tool_use/result que é ruído):
cat session.jsonl | jq -r 'select(.type=="user" or .type=="assistant") | .message.content'
```

### Critérios de minerar (mesmo do /save-vault)

Aplicar TODOS os critérios do `/save-vault` em cada sessão:
- Causa raiz antes de sintoma
- Específico > genérico  
- Português pt-BR
- Frontmatter com `updated: YYYY-MM-DD`
- Links Obsidian `[[arquivo]]` quando referenciar outro

---

## Edge cases

### Sessão muito curta (< 10 mensagens)

Provavelmente nada relevante. Reportar como "Sessão curta sem conteúdo significativo" e pular.

### Sessão duplicada (mesmo projeto, ambas ativas)

Pegar APENAS a mais recente (maior mtime). As outras provavelmente são abandonadas ou paralelas.

### Conversa ativa (modificada nos últimos 5min)

Provavelmente Valter ainda tá usando — perguntar antes:
"Sessão X foi modificada há 3min. Pode estar ativa. Processar mesmo assim?"

### Vault file-lock

Se 2 sessões processarem ao mesmo tempo, pode haver conflito. **Skill processa SEQUENCIALMENTE**, não em paralelo, pra evitar.

---

## Quando NÃO usar

- Quando rodando JUNTO com /save-vault em loop — escolha um
- Quando só uma sessão ativa — usa /save-vault que é mais leve
- Quando há trabalho não-confirmado (Valter pode querer continuar) — perguntar antes

---

## Conexão com outros skills

- **Substitui:** múltiplas chamadas de /save-vault
- **Não substitui:** `/checkpoint` (que é diferente — salva estado de TRABALHO em andamento)
- **Complementa:** atualização de MEMORY.md ao final
- **Pareado com `/bom-dia`** — `/boa-noite` salva pendências, `/bom-dia` retoma de onde parou

---

## OBRIGATÓRIO — Salvar estado pendente pra /bom-dia

Além do save-vault, salvar arquivo **`~/.claude/state/last-night.json`** com estrutura:

```json
{
  "savedAt": "2026-04-28T01:00:00Z",
  "sessions": [
    {
      "project": "Workspace | NodusHub",
      "projectPath": "/Users/valtersilva/Workspace | NodusHub",
      "jsonlPath": "/Users/valtersilva/.claude/projects/.../xxx.jsonl",
      "lastUserMessage": "última msg que ele mandou (truncada 200 chars)",
      "tasksOpen": [
        {"id": 9, "subject": "Re-disparar Wave Brasil", "status": "in_progress"}
      ],
      "nextActions": [
        "Ativar workflow N8N Olympus quando DNS propagar (~30min)",
        "Gravar criativo ads R$33/dia até quarta",
        "Validar score mail-tester após DNS propagar"
      ],
      "blockers": [
        "Aguardando senha de app gmail pra warmup",
        "Iris não testada com volume real — risco antes de ligar ads"
      ],
      "pendingDecisions": [
        "Sistema de indicação formal — criar mês 2?",
        "UI prospec botão 'Ligar' — fazer antes de segunda?"
      ]
    }
  ]
}
```

Como minerar cada campo do JSONL:
- **lastUserMessage**: última msg `role=user` antes do final
- **tasksOpen**: todas tasks com status != "completed" no `TaskList` da sessão
- **nextActions**: extrair de "🟡 PENDENTE", "próxima ação", "🟢 EM PROGRESSO" + lógica de leitura da última troca
- **blockers**: padrões "Aguardando X", "Falta Y", "Pendente Z"
- **pendingDecisions**: perguntas terminadas em "?" que assistant fez sem resposta do user

**Cria diretório se não existir:**
```bash
mkdir -p /Users/valtersilva/.claude/state
```

**Mantém histórico** em `~/.claude/state/last-night.YYYY-MM-DD.json` (cópia datada) pra `/bom-dia` poder olhar últimas N noites se quiser.
