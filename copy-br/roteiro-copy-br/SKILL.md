---
name: roteiro-copy-br
description: Skill de FLUXO INTERATIVO pra criar roteiros de vídeo curto (Reel, TikTok, Short, VSL curta). NUNCA escreve o roteiro de cara — sempre pergunta primeiro objetivo, formato, dor, antes de produzir. Metodologia baseada em Letícia Vaz (@leticiavazlv) adaptada pro contexto NodusHub/Olympus/Valter/clientes. Gatilhos obrigatórios PT-BR — "cria roteiro", "monta roteiro", "roteiro pra Reel", "roteiro de TikTok", "roteiro pra Short", "roteiro de vídeo", "script de Reel", "preciso de roteiro", "roteiriza isso", "transforma essa ideia em roteiro", "manda um roteiro pra mim", "roteiro de venda", "roteiro de conexão", "roteiro estratégico", "roteiro de Stories", "estrutura de roteiro", "como faço o roteiro pra", "roteiro do zero". Tem PRECEDÊNCIA sobre humanize-copy-br e hooks-copy-br quando o pedido é PRODUZIR roteiro (não corrigir voz nem só gancho). DELEGA: hook → hooks-copy-br | voz final → humanize-copy-br | persuasão/oferta → persuade-copy-br. NÃO usar pra: corrigir roteiro pronto (usa humanize-copy-br), só gancho solto (hooks-copy-br), legenda estática de post (copy-nodus ou tom-valter).
version: 1.0
created: 2026-05-22
metodologia: Letícia Vaz (@leticiavazlv) — TikTok 7642749704429784338
---

# roteiro-copy-br — Fluxo Interativo de Roteiro

> **Regra de ouro inviolável:** essa skill NUNCA produz roteiro sem antes passar pelo fluxo de perguntas. Atalho = roteiro genérico = lixo. Se o Valter já entregou todas as respostas no prompt inicial, pula pra produção. Se faltar 1, pergunta.

---

## Por que essa skill existe

`humanize-copy-br` cuida da VOZ. `hooks-copy-br` cuida do GANCHO. `persuade-copy-br` cuida do CONVENCIMENTO. Nenhuma delas decide O QUE DIZER. Essa skill é o **planejador estratégico** que define a arquitetura do roteiro ANTES de qualquer palavra ser escrita.

Sequência canônica:
1. `roteiro-copy-br` decide arquitetura (objetivo, formato, hook conceitual, 4 etapas)
2. `hooks-copy-br` polimento do gancho de abertura
3. Texto base produzido
4. `humanize-copy-br` aplicado por cima (voz, banwords, fluência oral)
5. `persuade-copy-br` aplicado se houver intenção de venda

---

## INVIOLÁVEIS

### 1. Sempre perguntar antes de produzir
Mínimo 4 perguntas respondidas antes da primeira linha de roteiro. Pode ser na mesma mensagem ou em interação. Se prompt inicial cobrir todas, pula direto pra produção.

### 2. Objetivo é o primeiro fork
Tudo deriva dele. Roteiro de Crescimento ≠ roteiro de Conversão. Não dá pra escrever sem saber.

### 3. Virada é etapa OBRIGATÓRIA em peças de Conversão/Conexão
A Virada é o que separa peça acusatória ("você que não sabe") de peça libertadora ("você que não teve acesso ao método certo"). Pular a Virada = peça que faz o espectador se sentir culpado = baixa conversão.

### 4. Hook nasce da DOR, nunca do tema
Errado: "Hoje vou falar sobre tráfego pago" (tema).
Certo: "Você gasta R$3 mil/mês com agência e não sabe se gerou paciente" (dor concreta).

### 5. CTA é específico, não genérico
"Comenta aí" sem motivo = morto. "Comenta CAIXA-PRETA que eu te mando o áudio explicando" = vivo.

### 6. Delegação obrigatória no fim
Roteiro produzido por essa skill SEMPRE passa por:
- `humanize-copy-br` (zerar cara de IA, banwords, oralidade)
- `persuade-copy-br` (se intenção for venda/conversão)
- `tom-valter` (se emissor for Valter pessoa)
- skill do cliente (se for Brenda, Olympus, etc.)

### 7. Quando emissor é Valter pessoa: PRIMEIRA PESSOA + VIVÊNCIA DECLARADA (INVIOLÁVEL)
Roteiro do Valter NUNCA pode ser narrador genérico falando verdade abstrata. Independente do tema (Crescimento, Conexão, Conversão, Retenção), tem que ter:
- **Primeira pessoa** ("eu", "meu", "comigo") em pelo menos 3 dos 5 blocos (Hook, Dor, Virada, Revelação/Produto, Ação).
- **Vivência declarada** — algo que o Valter REALMENTE viu, fez, pensou, deixou de fazer. Pode ser observação do círculo dele ("todo amigo empreendedor meu", "eu vi cliente meu fazer X"), pode ser decisão ("eu não contratei", "eu parei de fazer X"), pode ser opinião declarada ("eu acho que X é bobagem porque vi Y").
- **Opinião pessoal explícita**, não consenso de mercado. "Eu acho", "pra mim", "eu defendo", "no meu caso" no lugar de "estudos mostram", "todo mundo sabe", "a verdade é".

Anti-pattern: "A galera tá fazendo X" / "Você abre um negócio e pensa Y" / "Hoje uma pessoa faz Z". Tudo isso é template motivacional impessoal e queima a peça quando o emissor é o Valter.

Correção: "Eu olho pros meus amigos empreendedores fazendo X" / "Quando eu abri minha empresa eu pensei Y" / "Hoje eu opero Z sozinho".

---

## FLUXO DE PERGUNTAS (em ordem)

### Pergunta 1 — Objetivo
> Qual o objetivo desse vídeo?
>
> **A) Crescimento** — topo de funil. Generalista. Algoritmo distribui pra quem não te segue. Métrica = views, alcance, novos seguidores.
>
> **B) Conexão** — meio de funil. Cria desejo, mostra bastidor, prova social. Métrica = comentário qualificado, save, share.
>
> **C) Conversão** — fundo de funil. Quebra objeção, mostra produto aplicado. Métrica = clique no link, DM, agendamento.
>
> **D) Retenção** — cliente já dentro. Resultado, upsell, expansão, recompra. Métrica = LTV, recompra, NPS.

### Pergunta 2 — Emissor
> Quem fala nesse roteiro?
>
> - Valter pessoa (perfil @valterjuniorsilv)
> - NodusHub institucional
> - Olympus produto
> - Brenda Studio Renova
> - Outro cliente NodusHub (qual?)

### Pergunta 3 — Tema/Produto/Serviço
> O que vai divulgar nesse vídeo?
> Pode ser produto específico, serviço, campanha, ideia/conteúdo puro, ou só "conexão sem oferta".

### Pergunta 4 — Dor real
> Qual a DOR CONCRETA do espectador desse vídeo?
> Não é "ele não sabe X". É "ele já tentou X 3 vezes, perdeu R$Y, e agora desconfia de Z". Quanto mais específico, melhor o hook.

### Pergunta 5 (opcional) — Formato
Se não foi mencionado, sugerir baseado no objetivo:

**Crescimento** → Tutorial curto · Tela verde com print · Hot take · ASMR ferramenta · Comparativo "isso vs aquilo" · Mito vs verdade
**Conexão** → Bastidor real · Storytime · Resposta a comentário · Antes/depois · Conversa com cliente · Construindo em público
**Conversão** → Demo de produto · Estudo de caso nomeado · Quebra de objeção direta · Garantia explicada · Diferencial vs concorrente · Oferta + urgência
**Retenção** → Update de resultado · Tutorial avançado · Comunidade · Convite pra próximo passo

16 formatos canônicos: Talking head · React com tela verde · Tutorial passo-a-passo · ASMR de ferramenta · Bastidor · Storytime · Hot take · Mito vs verdade · Antes/depois · Comparativo "qual vale mais" · Estudo de caso · Demo de produto · Resposta a comentário · UGC fake · Carta aberta · Construindo em público.

### Pergunta 6 (opcional) — Duração e canal
Se não claro: Reel/TikTok ~30-45s · Short ~60s · VSL curta 90-180s · Carrossel falado ~15s por slide.

---

## ESTRUTURA DE ROTEIRO (4 etapas + Hook)

### HOOK (1-3s)
- Nasce da Dor da Pergunta 4
- 3 frames simultâneos: visual + texto na tela + voz
- Pra Valter pessoa: postura, nunca auto-desqualificação ("ainda não fechei", "tô tentando" — proibido)
- Delega refinamento pra `hooks-copy-br`

### ETAPA 1 — DOR (5-10s)
Espelha a Pergunta 4 amplificada. O espectador precisa pensar "ele tá falando comigo". Concreto, numérico se possível, sensorial.

### ETAPA 2 — VIRADA (obrigatória em Conversão/Conexão) (5-10s)
Reframe que tira a culpa do espectador. Estrutura: "Não é que você [acusação comum]. É que você [reframe libertador]".

Exemplos canônicos:
- "Não é que dentista não sabe vender. É que dentista nunca foi treinado pra vender — escola de odonto não ensina isso."
- "Não é que o tráfego não funciona. É que tráfego sem CRM e sem bot é só metade do sistema."
- "Não é que tua agência é ruim. É que o modelo de agência genérica não cabe mais em odontologia."

Pra Crescimento: Virada pode ser substituída por **Revelação** (informação contraintuitiva). Pra Retenção: substituída por **Update** (resultado novo).

### ETAPA 3 — PRODUTO/CONTEÚDO (10-20s)
Apresenta a solução como resposta NATURAL à Virada. Não vende — mostra. Se o conteúdo é a metodologia (educacional), entrega ali mesmo o passo prático. Loop cognitivo: o vídeo É o exemplo da metodologia funcionando.

### ETAPA 4 — AÇÃO (3-5s)
CTA ESPECÍFICO. Não "comenta aí". Sempre com motivo.
- Crescimento → "Salva esse pra não perder" / "Comenta qual desses 3 mais aconteceu com você"
- Conexão → "Me responde no DM se quer ver o próximo passo"
- Conversão → "Comenta CAIXA-PRETA que eu te mando o áudio explicando" / "Link na bio agora"
- Retenção → "Marca outro [cliente/colega] que precisa ver isso"

---

## TEMPLATE DE SAÍDA

Quando produzir o roteiro, sempre nesse formato:

```
R[NN] · [Objetivo] · [Formato]
─────────────────────────────

[HOOK 0-3s]
VISUAL: [o que aparece na tela]
TEXTO ON-SCREEN: [se houver]
VOZ: [fala]

[ETAPA 1 — DOR · 5-10s]
[fala contínua, oralidade — sem fragmentar]

[ETAPA 2 — VIRADA · 5-10s]
[Não é que X. É que Y.]

[ETAPA 3 — PRODUTO/CONTEÚDO · 10-20s]
[demonstra ou explica método]

[ETAPA 4 — AÇÃO · 3-5s]
CTA: [específico, com motivo]

─────────────────────────────
LEGENDA SUGERIDA: [primeira linha que aparece antes do "mais"]
HASHTAGS: [3-5 nicho, evitar genéricas]
TRILHA: [tendência ou voz própria — pra Brenda/nail, ver regra músicas autorais]
```

---

## REGRAS DE COMPOSIÇÃO COM OUTRAS SKILLS

| Situação | Skills que rodam em cascata |
|---|---|
| Roteiro Valter pessoa | `roteiro-copy-br` → `hooks-copy-br` → `tom-valter` → `humanize-copy-br` |
| Roteiro Conversão Olympus | `roteiro-copy-br` → `hooks-copy-br` → `persuade-copy-br` → `humanize-copy-br` |
| Roteiro Brenda nail | `roteiro-copy-br` → `hooks-copy-br` → skill Brenda (se houver) → `humanize-copy-br` |
| Roteiro Crescimento NodusHub | `roteiro-copy-br` → `hooks-copy-br` → `copy-nodus` → `humanize-copy-br` |
| Roteiro educacional puro (sem venda) | `roteiro-copy-br` → `hooks-copy-br` → `humanize-copy-br` (skipa persuade) |

---

## ANTI-PATTERNS (NÃO FAZER)

1. **Escrever sem perguntar.** Atalho = genérico = lixo.
2. **Pular Virada em peça de Conversão.** Vira peça acusatória.
3. **Hook baseado em tema, não dor.** "Vou falar sobre X" mata a peça.
4. **CTA genérico.** "Comenta aí" sem motivo = morto.
5. **Auto-desqualificação no hook do Valter.** "Ainda não fechei", "tô tentando" — proibido pela regra de postura.
6. **Inventar dado.** Se não tem o número real, genericiza ou pergunta antes (regra zero-invenção).
7. **Fragmentar fala em frases curtas só pra "variar ritmo".** Talking head é fala contínua — vírgula respira, ponto fecha ideia (regra ritmo-talking-head).
8. **Promete e não entrega na mesma peça.** Tipo "16 formatos diferentes" sem listar — funciona pra série, mata peça única.
9. **Soft sell mal disfarçado.** "Não vou vender nada mas eu poderia" — ou vende ou não menciona.
10. **Aplicar estrutura de 4 etapas em peça de bastidor puro.** Bastidor tem outra arquitetura (gancho de cena + contexto + revelação).

---

## EXEMPLO COMPLETO (peça real Olympus, Conversão)

**Respostas do briefing:**
- Objetivo: Conversão (dentista qualificado pra reunião)
- Emissor: Valter pessoa
- Tema: Olympus pacote R$1.797
- Dor: dentista já pagou R$3-5k em agência e não viu paciente entrar
- Formato: Talking head + texto na tela
- Duração: 35s Reel

**Roteiro produzido:**

```
R-OLYMPUS-CONVERSAO-01 · Conversão · Talking head

[HOOK 0-3s]
VISUAL: Valter olhando câmera, fundo terroso opaco, plano fechado.
TEXTO ON-SCREEN: "R$3 a 5 mil por mês. Quantos pacientes entraram?"
VOZ: Se você paga agência de tráfego e não consegue me responder na hora quantos pacientes ela trouxe, presta atenção.

[ETAPA 1 — DOR · 8s]
Eu já ouvi essa história de uns 30 dentistas. Contrata agência genérica, paga R$3 a R$5 mil por mês, vê dashboard bonito, mas na cadeira não chega ninguém novo. Aí o contador pergunta de onde veio o aumento de R$3 mil no custo fixo e você não sabe responder.

[ETAPA 2 — VIRADA · 7s]
Não é que tráfego pago não funciona em odontologia. É que ninguém te explicou que tráfego sozinho é metade do sistema. A outra metade é CRM, bot e um processo de qualificação que pega o lead do anúncio e leva até a cadeira sem você precisar correr atrás.

[ETAPA 3 — PRODUTO · 12s]
Eu juntei essas duas metades em uma stack só. Anúncio, bot WhatsApp e CRM rodando no mesmo trilho, com relatório semanal mostrando paciente por paciente. Custa R$1.797 por mês, contrato sem multa por 60 dias. Se em 60 dias não trouxer paciente, você sai e devolvo o último mês.

[ETAPA 4 — AÇÃO · 5s]
CTA: Comenta CAIXA-PRETA que eu te mando um áudio de 2 minutos com a matemática completa. Ou link na bio agora.

─────────────────────────────
LEGENDA SUGERIDA: A agência que você paga não te diz quantos pacientes entraram. A minha diz.
HASHTAGS: #odontologia #marketingodontologico #gestaodeconsultorio
TRILHA: voz própria (sem trilha)
```

---

## CRÉDITO METODOLÓGICO

Estrutura base derivada de Letícia Vaz (@leticiavazlv) — TikTok ID 7642749704429784338 (2026-05-22).

Adaptações NodusHub:
- 4 objetivos em vez de 3 (incluído Retenção)
- 16 formatos catalogados
- Composição obrigatória com skills humanize/hooks/persuade/tom-valter
- Regras anti-pattern específicas do contexto Valter (postura, zero-invenção, ritmo talking head)
- Exemplo completo com Olympus

---

**Versão:** 1.0 (2026-05-22)
