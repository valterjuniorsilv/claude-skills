---
name: brain
description: Vault deep-search. Quando o Valter rodar /brain <tema> ou disser "puxa tudo do vault sobre X", "me dá o brain do tema Y", "acessa o vault e me traz tudo de Z", "compila o conhecimento sobre W" — esta skill faz busca exaustiva no vault (multi-pass grep + leitura de notas relacionadas) e devolve um briefing denso com todo conteúdo relevante. Use SEMPRE que o Valter quiser carregar contexto profundo de um tema antes de começar a trabalhar nele.
---

# /brain — Vault Deep-Search

> Carrega TUDO que o vault tem sobre um tema, em uma passagem só, antes de iniciar qualquer trabalho.

---

## Quando ativar

Gatilhos canônicos:
- `/brain <tema>`
- "puxa tudo do vault sobre X"
- "me dá o brain do tema Y"
- "compila tudo sobre Z"
- "carrega contexto de W"
- "o que o vault tem sobre A"

Diferença pra `vault-first`:
- `vault-first` = busca rasa antes de executar uma entrega
- `/brain` = **dump completo** do vault sobre o tema, sem entregar nada — só carrega contexto profundo

---

## Protocolo de execução

### 1. Extrair termos-chave do tema

Identificar 3-7 termos relacionados ao tema. Exemplos:
- Tema "SAARA" → `saara`, `atendente`, `iris`, `whatsapp`, `bot`, `qualificação`
- Tema "paleta dark" → `paleta`, `warm black`, `silver`, `neutral`, `dark ui`, `cor`
- Tema "Olympus odonto" → `olympus`, `odonto`, `dentista`, `clínica`, `crc`
- Tema "tráfego pago" → `tráfego`, `meta ads`, `cpl`, `ctwa`, `criativo`

### 2. Busca multi-pass

Vault root: `/Users/valtersilva/Documents/Obsidian Vault/`

Pass 1 — busca por nome de arquivo:
```bash
find "$VAULT" -iname "*<termo1>*" -o -iname "*<termo2>*" 2>/dev/null
```

Pass 2 — busca por tag YAML:
```bash
grep -rln "tags:.*<termo>" "$VAULT" 2>/dev/null
```

Pass 3 — busca por conteúdo (case-insensitive):
```bash
grep -rln -i "<termo>" "$VAULT" 2>/dev/null
```

Pass 4 — busca por wikilinks `[[<termo>]]`:
```bash
grep -rln "\[\[.*<termo>" "$VAULT" 2>/dev/null
```

Mergir resultados, deduplicar por path, ordenar por relevância (matches por arquivo).

### 3. Identificar arquivos canônicos primeiro

Priorizar notas com status `canônico` ou `CANONICAL` no frontmatter — essas são a fonte de verdade atual. Arquivos `deprecated` vão pro final ou são citados como histórico.

```bash
# Top tier: canônicos
grep -l "status:.*[Cc]an" <found-files>

# Bottom tier: deprecated  
grep -l "DEPRECATED\|deprecated" <found-files>
```

### 4. Ler os arquivos prioritários inteiros

Ler TOP 5-10 arquivos mais relevantes inteiros (não só excerpt). Pra arquivos longos (>500 linhas), ler primeiras 200 + tabela de conteúdo + seções marcadas como canônicas.

### 5. Seguir wikilinks transitivos

Pegar `[[NomeDoLink]]` mencionados nos arquivos lidos. Se aparecer 2+ vezes em arquivos diferentes, é importante — abrir e ler.

### 6. Mapear índice MEMORY.md

Sempre checar `~/.claude/projects/-Users-valtersilva-Workspace---NodusHub/memory/MEMORY.md` — tem ponteiros pra sessões anteriores que tocaram o tema.

### 7. Sintetizar e devolver

Formato de resposta:

```markdown
## Brain dump: <tema>

### Status canônico atual
[arquivo principal canonizado + 1 frase do que define]

### Decisões já tomadas
- [decisão 1] em [arquivo] — [contexto curto]
- [decisão 2] em [arquivo] — [contexto curto]

### Frameworks/receitas reusáveis
- [framework X] em [arquivo:linha]
- [framework Y] em [arquivo:linha]

### Bugs/aprendizados já vividos
- [bug ou armadilha] em [arquivo]

### Estado em prod (se aplicável)
- [URL, endpoint, env vars relevantes]

### Histórico/deprecated (não usar, só pra contexto)
- [arquivo deprecated] — substituído por [novo]

### Links transitivos relevantes (pra abrir depois se quiser)
- [[link1]] · [[link2]] · [[link3]]

### Arquivos lidos integralmente
1. <path1>
2. <path2>
...
```

---

## Princípios

1. **Exaustividade > brevidade.** Se o Valter pediu /brain, quer profundidade. Não corte.
2. **Hierarquia: canônico > deprecated > histórico.** Sempre dizer qual é a verdade atual.
3. **Cite arquivos com path completo** pra ele poder abrir no Obsidian.
4. **Não sintetize demais.** Trazer exemplos concretos, hex values, frameworks completos — não resumos vagos.
5. **Distinguir conhecimento de opinião.** Marcar [vault canônico] vs [minha leitura].
6. **Não execute o trabalho.** /brain só carrega contexto. Trabalho vem em comando separado.

---

## Anti-patterns

- ❌ Devolver só 3 bullets quando o vault tem 15 notas sobre o tema
- ❌ Ignorar arquivos `deprecated` (eles têm contexto de "por que mudou")
- ❌ Citar arquivos sem path completo
- ❌ Pular o MEMORY.md (tem ponteiros importantes)
- ❌ Resumir frameworks sem dar exemplos concretos
- ❌ Começar a executar o trabalho do tema — /brain SÓ carrega contexto

---

## Exemplo de uso

```
Valter: /brain SAARA
```

Resposta esperada:
```markdown
## Brain dump: SAARA

### Status canônico atual
`Projetos/SAARA-Atendente-Olympus.md` — SAARA é Sistema de Atendimento Automatizado 
Responsivo e Adaptativo, atendente IA do Olympus que opera WhatsApp 24/7...

### Decisões já tomadas
- Nome canonizado SAARA em 2026-05-XX, superseding "SAA" técnico em [[SAA-Sistema-Atendimento-Automatizado]]
- Atendente por cliente: nome custom (Mariana, Júlia) na visão do paciente, SAARA no institucional
- Workflow N8N separado por nicho (odonto = `iris-bot/workflow-odonto.json`)

### Frameworks reusáveis
- SPIN 13 perguntas em `services/iris-bot/nodes/...`
- Anti-dup hash SHA1 em workflow N8N (patch 2026-05-22)

### Bugs vividos
- @lid expira ~horas → mensagens manuais ficam PENDING (vault: Olympus-CRM-Cliente §known-issue)
- Cross-routing Iris (startsWith match) — fix v2 em workflow-odonto.json

### Estado em prod
- CAPI Lead/Schedule LIVE em `capi.olympusodonto.com.br/capi/olympus/lead-qualified`
- Workflow N8N: instance `iris-olympus`
- Bot rodando: Hetzner Docker container N8N

### Histórico/deprecated
- `SAA-Sistema-Atendimento-Automatizado.md` — sigla técnica, ainda válida mas em material novo usa SAARA

### Wikilinks transitivos
[[Iris-Odonto-Workflow-Separado]] · [[CAPI-Lead-Schedule-Olympus-LIVE-2026-05-22]] · [[Olympus-CRM-Cliente]]
```

---

## Configuração

- Vault path: `/Users/valtersilva/Documents/Obsidian Vault/`
- MEMORY.md path: `/Users/valtersilva/.claude/projects/-Users-valtersilva-Workspace---NodusHub/memory/MEMORY.md`
- Encoding: UTF-8 (suporta acentos)
- Skip dirs: `.obsidian/`, `.trash/`, `node_modules/`

---

## Documentos com prioridade absoluta (sempre ler PRIMEIRO se tema bater)

Arquivos com `prioridade_brain: 1` no frontmatter são fonte de verdade absoluta. Se o tema do /brain bater com a área coberta por um desses, ler ele INTEIRO antes de qualquer outro:

| Tema disparador | Arquivo canonical |
|---|---|
| Olympus, identidade, brand, paleta, logo, tipografia, cor, Cabinet Grotesk, design system Olympus, tokens Olympus, visual Olympus | `Design/Olympus-Brand-Book-CANONICAL.md` |

**Regra de ouro:** quando o /brain bater no tema Olympus identidade, **NUNCA** consultar `Olympus-Brand-Paleta-2026-05-17.md`, `Olympus-Paleta-Warm-Black-2026-05-22.md`, `Olympus-Paleta-True-Neutral-2026-05-23.md`, `Olympus-Sistema-Visual-Ads.md`, ou `Olympus-Visual-Instagram.md` §paleta — todos foram SUPERSEDED pelo Brand Book CANONICAL. Eles ficam só como histórico de evolução.

Pra adicionar novos canonical masters:
1. Frontmatter: `prioridade_brain: 1` + `aliases: [lista de termos]`
2. Status: `CANÔNICO ABSOLUTO`
3. Listar `supersedes` pra deprecar anteriores
