---
name: save-vault
description: Salva o conteúdo relevante da conversa atual no Obsidian Vault do Valter. Use SEMPRE que o Valter disser /save-vault, "salva no vault", "salva essa conversa", "guarda isso no vault", "registra no obsidian", ou qualquer variação. Também usar proativamente ao final de sessões que geraram conhecimento, estratégias, decisões ou aprendizados que merecem ser preservados para sessões futuras.
---

# /save-vault — Salvar no Obsidian Vault

## Objetivo

Extrair o que foi criado/decidido nesta conversa e salvar nos locais corretos do Obsidian Vault em `/Users/valtersilva/Documents/Obsidian Vault/`.

O vault é a fonte de verdade do Valter. Tudo que tem valor duradouro vai para lá. **Não um diário da sessão — uma base de conhecimento operacional.**

---

## O que VALE salvar (critérios duros)

### Bugs com causa raiz
Se um bug foi corrigido, salvar:
- **Sintoma** (o que o usuário via)
- **Causa raiz** (por que acontecia — não "código errado", mas o mecanismo específico)
- **Fix** (o que foi mudado e por quê isso resolve)
- **Como prevenir** (o que verificar antes de acontecer de novo)

Exemplo de causa raiz boa: "btoa() não suporta Unicode — 'Terça' com ç quebrava silenciosamente"
Exemplo ruim (não salvar): "bug corrigido no calendário"

### Decisões técnicas com trade-offs
Se uma abordagem foi escolhida sobre outra, salvar:
- Qual opção foi escolhida
- Por que essa e não as outras
- Limitações da escolha feita

Exemplo: "ICS gerado client-side (Blob) vs API — escolhido client-side: sem limite de URL, funciona offline, zero latência"

### Configurações e env vars descobertas
Qualquer variável de ambiente, chave de API, URL de webhook, configuração de servidor que foi encontrada ou configurada. Com contexto de onde fica e pra que serve.

Exemplo: "IG_PASSWORD_ENCRYPTION_KEY — 64 chars hex, obrigatória em creative-studio no Vercel, gerada com: openssl rand -hex 32"

### Padrões de código estabelecidos no projeto
Se um padrão foi criado ou consolidado nessa sessão (estrutura de pasta, convenção de nome, forma de fazer X), salvar com exemplo mínimo.

### URLs, rotas e endpoints ativos
Qualquer endpoint de API, webhook, URL de deploy que foi criado ou confirmado funcionando.

### Voz/tom/copy aprovado
Se o Valter aprovou um texto, hook, tom de voz, estrutura de copy — salvar com o exemplo concreto.

---

## O que NÃO salvar

- "Sessão produtiva, fizemos X, Y e Z" — isso é diário, não base de conhecimento
- Passos de debugging que não levaram a nada
- Código que vai estar no repositório (o repo é a fonte de verdade do código)
- Contexto óbvio que qualquer dev deduziria lendo o código
- Resumos genéricos sem dado específico
- Decisões que o Valter ainda não tomou

---

## Estrutura do Vault

```
Obsidian Vault/
├── Projetos/          → Estado atual de cada projeto (bugs, decisões, URLs)
├── Estrategias/       → Planos e estratégias de marketing, negócio, tráfego
├── Conceitos/         → Conhecimento técnico novo (ferramenta, padrão, framework)
├── Meta Ads/          → Conhecimento específico de Meta Ads
├── Meta Organico/     → Instagram orgânico, algoritmo, crescimento
├── Feedbacks/         → Correções de comportamento do Claude
├── Comercial/         → Estratégia comercial, precificação
├── Produtos/          → Detalhes dos produtos NodusHub
├── Design/            → Padrões visuais, templates
├── Setup-Claude/      → Configurações e regras do Claude
└── Sobre Mim/         → Perfil e contexto pessoal do Valter
```

Para projetos técnicos ativos (Creator Studio, Lode, Mine, Finance), usar `Projetos/[NomeProjeto].md` como arquivo principal que accumula estado ao longo do tempo.

---

## Processo de Salvamento

### 1. Minerar a conversa com olhar de engenheiro

Passar por TODA a conversa buscando especificamente:

- Qualquer `throw`, exceção ou erro com causa raiz identificada
- Qualquer variável de ambiente, URL, configuração mencionada
- Qualquer decisão técnica com "escolhi X porque Y"
- Qualquer padrão de código criado ("sempre fazer assim")
- Qualquer copy/hook aprovado pelo Valter
- Qualquer dado numérico concreto (limites, quotas, preços, métricas)
- Qualquer dependência entre sistemas descoberta

### 2. Verificar se já existe arquivo relacionado

Fazer `Glob` para checar antes de criar:
```
Glob: /Users/valtersilva/Documents/Obsidian Vault/Projetos/*Creator*
Glob: /Users/valtersilva/Documents/Obsidian Vault/Projetos/*Studio*
```

Se existir, **atualizar** o arquivo existente com seção nova — não criar duplicado.

### 3. Escrever com densidade máxima

**Frontmatter obrigatório:**
```markdown
---
tags: [tag1, tag2]
updated: YYYY-MM-DD
---
```

**Estrutura para arquivo de projeto:**
```markdown
# [Nome do Projeto] — Estado Técnico

## Bugs Resolvidos

### [Nome do Bug] (YYYY-MM-DD)
**Sintoma:** o que o usuário via
**Causa raiz:** mecanismo específico do problema
**Fix:** arquivo:linha — o que mudou
**Prevenir:** o que checar antes de acontecer de novo

## Decisões Técnicas

### [Nome da Decisão] (YYYY-MM-DD)
**Escolha:** [opção escolhida]
**Motivo:** [por quê essa e não outras]
**Limitação:** [o que a escolha não resolve]

## Configurações / Env Vars

| Var | Onde | Para que | Como gerar |
|-----|------|----------|------------|
| VAR_NAME | Vercel prod | descrição | comando |

## URLs e Endpoints Ativos

| Endpoint | URL | Método | Status |
|----------|-----|--------|--------|
```

**Nome do arquivo:** PascalCase, descritivo, sem espaços. Ex: `CreatorStudio-Tecnico.md`

### 4. Atualizar MEMORY.md do projeto

Após salvar no vault, verificar se `~/.claude/projects/[projeto]/memory/MEMORY.md` precisa de ponteiro novo ou atualização de estado.

### 5. Confirmar ao Valter

Formato conciso sem emojis:

```
Salvo no Vault:

Projetos/CreatorStudio-Tecnico.md — 3 bugs com causa raiz, 2 decisões técnicas, env vars
Meta Organico/Formatos-Virais-2026.md — atualizado com padrões de copy aprovados

MEMORY.md: atualizado
```

---

## Regras

- **Causa raiz antes de sintoma.** Um bug sem causa raiz registrada vai acontecer de novo.
- **Específico > genérico.** "btoa falha com Unicode" vale 10x mais que "bug de exportação corrigido".
- **Não duplicar.** Checar antes de criar.
- **Não resumir demais.** Estratégia completa → salvar completa.
- **Português.** Todo conteúdo do vault é pt-BR.
- **Links Obsidian.** Conectar com `[[nome-do-arquivo]]` quando mencionar outro arquivo do vault.
- **Data atualizada.** Campo `updated` = hoje.

---

## Exemplo de entrada de bug bem documentada

```markdown
### btoa() não suporta Unicode — exportação .ics (2026-04-11)
**Sintoma:** botão de exportar calendário aparecia habilitado mas não fazia nada
**Causa raiz:** `btoa(JSON.stringify(slots))` joga exceção silenciosa quando a string contém
caracteres não-ASCII (ç, ã, é em "Terça", "Ângulo", etc.). O erro era swallowed sem alert.
**Fix:** abandonar btoa completamente — gerar ICS inteiramente client-side com Blob:
  `new Blob([icsString], { type: 'text/calendar;charset=utf-8' })` → createObjectURL
**Prevenir:** nunca usar btoa() com strings que podem ter acentos. Usar TextEncoder ou Blob.
```

## Exemplo de entrada de decisão técnica

```markdown
### ICS gerado client-side vs endpoint de API (2026-04-11)
**Escolha:** Blob client-side — zero chamada de API
**Motivo:** Abordagem via GET /api/calendario/export?d=BASE64 falhou no Safari mobile
  (janela em branco). POST precisaria de fetch + blob que também tem bugs no Safari iOS.
  Gerar no cliente: sem limite de URL, sem round-trip, funciona offline, mais simples.
**Limitação:** se a lógica de geração de ICS mudar, só atualiza no frontend (não é API-first).
```
