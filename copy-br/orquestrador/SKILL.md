---
name: copy-br
description: Skill ORQUESTRADORA MASTER de copy do Valter Silva e NodusHub. Porta de entrada única que aciona o pipeline completo de produção de roteiro/copy em cascata determinística — roteiro-copy-br (briefing + estrutura) → hooks-copy-br (gancho) → persuade-copy-br (gatilhos, se venda) → humanize-copy-br (voz, anti-IA) → tom-valter (se emissor é Valter pessoa) OU copy-nodus (se institucional) OU skill cliente (Brenda/Olympus). Integra também `copiar-viral` em 2 momentos: como Modo Modelar (input = URL de vídeo viral em vez de briefing do zero) e como Auditoria final (checklist Oney 19 itens antes de entregar). Gatilhos PT-BR obrigatórios — "/copy-br", "passa pelo pipeline", "pipeline completo de copy", "roteiro pelo fluxo", "vai pelas skills", "fluxo de copy br", "monta tudo certinho", "passa pelas 4 skills", "cria roteiro pelo método", "skill mestra de copy", "passa essa frase pelo fluxo". PRECEDÊNCIA: quando invocada explicitamente, `copy-br` é a única skill que orquestra — as outras viram subordinadas em cascata. Quando NÃO invocada explicitamente, cada skill atua sozinha conforme gatilho próprio. NÃO usa pra: corrigir 1 frase isolada (humanize-copy-br direto), só pesquisar referência (vault-first), só design visual (brand-guidelines).
version: 1.0
created: 2026-05-23
relacionado:
  - roteiro-copy-br
  - hooks-copy-br
  - persuade-copy-br
  - humanize-copy-br
  - tom-valter
  - copy-nodus
  - copiar-viral
  - "[[Catalogo-Modelagem-TOF-MOF-BOF-2026-05-23]]"
  - "[[Banco-Frases-Tese-Onscreen-Valter-2026-05-23]]"
  - "[[Checklist-Oney-19-Itens]]"
---

# /copy-br — Skill Orquestradora Master de Copy

> Porta única de entrada pro pipeline completo de copy. Garante que NENHUMA peça de texto destinada a leitura humana saia sem passar por todas as camadas do stack NodusHub.

---

## Quando invocar

- Valter digita `/copy-br` ou variação dos gatilhos
- Pedido pra montar roteiro de Reel/TikTok/Short que vai precisar de pipeline completo
- Pedido "passa essa frase pelo fluxo" / "passa pelo pipeline"
- Toda vez que produzir uma peça que merece o nível máximo de cuidado

## Quando NÃO invocar

- Corrigir 1 frase isolada → `humanize-copy-br` direto
- Só gancho solto → `hooks-copy-br` direto
- Só pesquisar referência → `vault-first`
- Resposta de DM rápida → `tom-valter` direto
- Edição de copy existente que tá quase pronta → skill específica do estágio

---

## Princípio central

**Cascata determinística, não opcional.** Quando `copy-br` é invocada, o pipeline RODA TODAS as camadas aplicáveis. O modelo NÃO escolhe pular etapa. O usuário pode pular EXPLICITAMENTE ("já tenho o briefing, pula pra hooks") mas o default é rodar tudo.

---

## Pipeline canônico (2 modos)

### MODO A — Criar do zero (briefing → roteiro novo)

```
1. roteiro-copy-br           → Briefing 4 perguntas + esqueleto 4 etapas
   (Objetivo / Emissor / Tema / Dor + opcional Formato/Duração)

2. hooks-copy-br             → Polir gancho 0-3s (postura, gap, bomba semântica)

3. persuade-copy-br          → SE objetivo for Conversão/Conexão com intenção venda
                                (gatilhos Cialdini, anchoring, framing, oferta)
                                SE for Crescimento educacional puro → PULAR

4. humanize-copy-br          → Sempre. Zero IA, banwords, ritmo contínuo, sem travessão

5. tom-valter OU copy-nodus  → SE emissor é Valter pessoa → tom-valter
   OU skill cliente             SE emissor é NodusHub institucional → copy-nodus
                                SE emissor é Olympus produto → tom Olympus
                                SE emissor é Brenda → skill Brenda

6. AUDITORIA copiar-viral    → Checklist Oney 19 itens (rodar como verificação final)
   (modo audit, não criação)    Se 5+ itens falharem → voltar pro passo 4 e refazer
```

### MODO B — Modelar a partir de vídeo viral (URL como input)

Quando Valter cola URL de Reel/TikTok/Short pedindo pra modelar:

```
1. copiar-viral              → Recebe URL(s), baixa, transcreve, extrai engenharia
   (modo criação completo)      Já gera roteiro adaptado pra voz Valter via 9 princípios Ruiva

2. roteiro-copy-br           → Refina o output da copiar-viral aplicando regras invioláveis #7/#8
                                (1ª pessoa + vivência + generalista se topo)

3. hooks-copy-br             → Polir gancho ajustado

4. persuade-copy-br          → SE houver intenção de venda

5. humanize-copy-br          → Sempre

6. tom-valter OU outra       → Conforme emissor

7. AUDITORIA Oney            → Mesma do Modo A
```

---

## Onde `copiar-viral` entra (resposta direta à pergunta do Valter)

**Em 2 momentos distintos do pipeline:**

### Momento 1 — Como porta de entrada do MODO B

Quando o briefing **não vem de pergunta** e sim de **referência viral** (URL). Aí `copiar-viral` substitui as 4 perguntas do `roteiro-copy-br` — ela extrai estrutura direto do vídeo modelado. Depois entra `roteiro-copy-br` em modo "refinar saída", aplicando regras invioláveis #7 (1ª pessoa) e #8 (generalista se topo).

### Momento 2 — Como AUDITORIA pós-hoc (Modo A E Modo B)

Antes de entregar QUALQUER peça final, rodar o checklist Oney 19 itens (`[[Checklist-Oney-19-Itens]]`) que o `copiar-viral` codifica nos 9 princípios canônicos da Ruiva Especialista. Se 5+ falharem, regrava.

Isso torna `copiar-viral` o "controle de qualidade" do pipeline, não só o "criador alternativo".

---

## Outputs determinísticos

Toda invocação de `/copy-br` entrega:

```
1. BRIEFING (decisões registradas)
   - Objetivo / Emissor / Tema / Dor / Formato / Duração

2. ESQUELETO (4 etapas + hook)
   - Hook + Dor + Virada + Revelação/Produto + Ação

3. TEXTO PRONTO PRO TELEPROMPTER (corre limpo)
   - Texto sem markdown, parágrafos separados por idéia

4. TEXTOS ON-SCREEN (1 a 2 frases-bomba)
   - Frame zero (tese completa) + opcional meio do vídeo (reframe)

5. METADADOS
   - Duração estimada
   - Legenda sugerida (primeira linha visível antes do "...mais")
   - Hashtags (3-5 nicho, evitar genéricas)
   - Trilha sugerida

6. AUTO-CHECAGEM
   - Lista das invioláveis cumpridas + Oney 19 itens

7. PIPELINE LOG
   - Cada camada e o que mudou (transparente, auditável)
```

---

## Regras invioláveis herdadas

`copy-br` herda E faz cumprir TODAS as invioláveis das skills filhas:

**De `roteiro-copy-br`:**
- #7 Emissor Valter pessoa → 1ª pessoa + vivência declarada em ≥3 dos 5 blocos
- #8 Crescimento topo → generalista, não nicho odonto

**De `humanize-copy-br`:**
- Zero travessão
- Zero banwords (crucial, robusto, comprehensive, fundamental, jornada, etc)
- Ritmo talking head contínuo
- Sem auto-desqualificação no hook

**De `hooks-copy-br`:**
- Hook nasce da dor, nunca do tema
- Promessa de payoff específico
- Gap de informação fechado

**De `persuade-copy-br`:**
- Gatilho sobre voz humanizada, nunca em texto IA
- Anchoring com número verificável
- Anti-promessa exagerada

**De `tom-valter` (se Valter pessoa):**
- Mineiro maduro, anti-guru
- Específico nos números (que sejam reais)
- Admite limite no corpo, NUNCA no gancho

**Zero invenção (regra meta NodusHub):**
- Nunca cravar cliente, número, episódio ou caso que não exista
- Contrafactual permitido se marcado ("se eu tivesse...", "seria...")

---

## Logging e transparência

A cada invocação, mostrar no fim:

```
─── PIPELINE LOG ───
✓ roteiro-copy-br: briefing capturado, esqueleto 4 etapas gerado
✓ hooks-copy-br: hook polido (mudança: X → Y, razão Z)
✓ persuade-copy-br: gatilhos aplicados (anchoring, loss aversion)
○ tom-valter: aplicado (4/5 blocos com 1ª pessoa)
○ humanize-copy-br: zero travessão, zero banwords, ritmo contínuo
✓ AUDITORIA Oney 19: 18/19 passou (item X falhou → corrigido)
```

Isso ensina o Valter o que cada camada faz E permite ele ver onde queimou.

---

## Atalho: pular etapas explicitamente

Valter pode mandar:
- `/copy-br pula briefing, tema é X, dor é Y` → entra direto na produção
- `/copy-br só humanize` → equivale a chamar `humanize-copy-br` direto
- `/copy-br modela esse link [URL]` → ativa Modo B explicitamente
- `/copy-br audita essa peça [texto]` → roda só auditoria Oney sobre texto existente

---

## Composição com outras skills NodusHub

- `vault-first` SEMPRE roda antes do passo 1 — busca referências (frase-tese, voz, vivência) no vault
- `nodus-orchestrator` pode invocar `copy-br` quando tarefa tem ≥2 peças paralelas (ex: roteiro + carrossel + legenda)
- `nodus-agent-memory` salva learnings de cada execução pro próximo lote ficar mais inteligente

---

## Exemplo de invocação completa (Modo A)

**Valter:** "/copy-br monta roteiro pra Reel sobre IA aplicada"

**Eu (executando):**

1. Invoco `vault-first` → busco "IA aplicada" + tom Valter no vault
2. Invoco `roteiro-copy-br` → faço as 4 perguntas (objetivo, emissor, tema, dor)
3. Valter responde
4. Produzo esqueleto 4 etapas
5. Invoco `hooks-copy-br` → polo o gancho
6. Avalio objetivo: se for Conversão → invoco `persuade-copy-br`. Se for Crescimento → pulo
7. Invoco `humanize-copy-br` → aplico voz, banwords, ritmo
8. Avalio emissor: Valter pessoa → invoco `tom-valter` e checo invioláveis #7/#8
9. Rodo auditoria Oney 19 → corrijo o que falhar
10. Entrego output determinístico (briefing + esqueleto + teleprompter + on-screen + metadados + pipeline log)
11. Invoco `nodus-agent-memory` pra salvar learnings

---

## Versão e mudanças

- **v1.0 (2026-05-23):** criada após sessão de modelagem Roberth + auditoria do banco de 20 frases. Consolida cascata que antes vivia distribuída entre skills filhas.
