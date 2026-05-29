---
name: persuade-copy-br
description: Skill MOTOR de persuasão e convencimento para copy NodusHub/Olympus/Valter/clientes. Aplica gatilhos mentais, neuromarketing e estrutura de oferta SOBRE a voz humana já calibrada por `humanize-copy-br`. Gatilhos obrigatórios PT-BR — "como vender", "gatilho mental", "aumentar conversão", "framing", "estrutura de oferta", "oferta irresistível", "tratar objeção", "responder objeção", "CTA pra", "CTA persuasivo", "escassez real", "autoridade", "urgência", "storytelling de venda", "VSL", "carta de venda", "headline persuasiva", "Cialdini", "neuromarketing", "social proof", "como convencer", "fechar venda", "PAS", "AIDA", "BAB", "PASTOR", "anchoring", "loss aversion", "future pacing", "stack de valor", "garantia condicional", "risk reversal", "Hormozi", "Sabri Suby", "big idea". COMPLEMENTA humanize-copy-br: humanize define a VOZ (zero IA, 12 invioláveis), persuade define a ESTRUTURA de convencimento. Roda DEPOIS de humanize sempre que a peça tem intenção de venda, conversão ou tratamento de objeção. NÃO substitui humanize: gatilho mal aplicado em voz de IA = duplo cringe. Tem precedência sobre `copy-humana`, `marketing-copy` e `copywriting` quando o objetivo é convencer/vender no contexto NodusHub.
tags: [persuasao, neuromarketing, gatilhos, copy, canonical, br, vendas, conversao]
---

# Copy Persuasiva BR Canônica — Motor de Convencimento

> Esta skill é o MOTOR. `humanize-copy-br` é o ACABAMENTO. Hooks-copy-br é a PORTA. As três camadas trabalham juntas: hook abre, persuade convence, humanize entrega na voz que não tem cara de IA. Pra teoria profunda, consulte `Conceitos/Neuromarketing-Persuasao-2026.md` (1461 linhas) e os 3 docs canônicos listados na seção 13.

---

## 0. INVIOLÁVEL — Persuasão honesta, sempre

Estas 12 regras NÃO admitem exceção. Persuasão desonesta funciona uma vez e queima o emissor. Tudo aqui é arquitetura invisível: se o leitor SENTE o gatilho, o gatilho falhou.

1. **Escassez SEMPRE real.** "4 vagas Founding Member com CNPJ assinado" sim. "Últimas vagas, corre!" eterno no site não. Escassez fabricada é o gatilho mais detectado pelo público BR 2026. Ver Neuromarketing §2.6.
2. **Urgência SEMPRE com data específica.** "Encerra sexta 23/05 às 23h59" sim. "Por tempo limitado" não. Se não tem data real, não usa urgência.
3. **Loss aversion SEMPRE com perda mensurável.** "Você perdeu 8 pacientes particulares em maio, R$24 mil em receita" sim. "Não perca essa oportunidade" não. Ver §1.3.
4. **Autoridade SEMPRE demonstrada, não declarada.** "Construí o sistema que roda na minha esposa, R$30/dia, conta act_459091013859000, 18 conversas em 30 dias" sim. "Especialista certificado em tráfego pago" não. Ver §2.5.
5. **Garantia SEMPRE blindada juridicamente.** Condicional, escrita, com gatilho objetivo de acionamento. "3 primeiros meses sem fidelidade, cancela sem multa por escrito" sim. "Garantia de satisfação total" não. Crossover com humanize §garantia processual.
6. **Big number SEMPRE auditável.** "R$241,36 / 7 conversas / 0 handoff em 7d" sim. "R$50 milhões geridos" sem cliente nomeado não. Se você não pode provar com print/contrato/conta, não escreve.
7. **Anchoring SEMPRE com referência real.** "Agência cobra R$5-15k/mês. Olympus R$1.797" sim. "De R$9.997 por R$97" (preço de mentira) não. Ver §1.7.
8. **Storytelling SEMPRE com nome, hora, local.** "Caroline, Brenda Studio Renova, Mandaguaçu PR, terça 14h" sim. "Uma cliente nossa transformou o negócio" não. Ver §6.
9. **Objeção SEMPRE responde lógica E medo.** "Tá caro" não é só matemática, é medo de errar de novo. Resposta precisa cobrir os dois. Ver §8.
10. **CTA SEMPRE específico e baixo atrito.** "Quero conversar com o Valter quarta 14h" sim. "Saiba mais" / "Garanta já o seu" não. Ver §9.
11. **Pre-suasion ANTES de oferta.** Quem o leitor é (identity), com quem ele tá (tribo), o que ele perdeu (loss), só DEPOIS o que você oferece. Cialdini 2016 — quem oferece sem preparar o terreno mental queima conversão. Ver §2.7.
12. **Auto-policia obrigatória.** Antes de entregar, checklist da seção 8 + grep mental por gatilho fabricado/cringe + leitura no teste do bar (herdada de humanize §0.7).

---

## 1. Quando ativar esta skill

ATIVAR sempre que a peça tem **intenção de convencer ou vender**:

- Headline persuasiva (Meta, Google, LP)
- CTA de qualquer canal
- VSL / carta de venda
- Sequência de email (cold → quente)
- Página de oferta de produto/serviço
- Tratamento de objeção (post, email, DM)
- Storytelling de venda
- Estruturação de pitch / proposta comercial
- Reescrita pra aumentar conversão de peça existente
- Reativação de lead dormido com nova âncora
- Pitch de reunião 1:1 com lead quente
- Anúncio de lançamento / vaga aberta / oferta nova
- Página de obrigado com upsell

NÃO ativar pra:

- Copy de aquecimento sem oferta (post de bastidor, educativo puro) → vai trair se forçar gatilho
- Atendimento técnico (Iris respondendo dúvida operacional)
- Comunicação interna NodusHub
- Resposta genérica a comentário sem CTA
- Conteúdo educativo puro (autoridade vem da demonstração, não da venda)
- Code, commit, doc técnica

**Regra-mestra:** se a peça precisa que o leitor TOME UMA AÇÃO específica, ativa. Se a peça só planta tese ou entrega utilidade sem pedir nada, não ativa.

---

## 2. Fluxo de execução (não pule passos)

1. **Discovery de contexto** (seção 2.5). Verifica 4 dimensões críticas da humanize + 3 dimensões específicas de persuasão (estágio de consciência, temperatura, prova disponível).
2. **Identifica emissor + skill secundária** (puxa calibração da humanize §7).
3. **Identifica estágio de consciência (Schwartz) e temperatura** do leitor (Unaware → Most-aware × Frio → Cliente atual).
4. **Seleciona gatilho(s) apropriado(s)** — seção 3. Cada estágio aceita gatilhos diferentes.
5. **Estrutura o argumento** — escolhe framework (PAS / AIDA / BAB / PASTOR / SB7 / 4Ps / Sabri Godfather) — seção 5.
6. **Escreve V1** já passando por `humanize-copy-br` (zero travessão, zero banword, voz do emissor).
7. **Roda auto-policia** (seção 8): toda promessa tem prova? toda escassez é real? gatilho ficou invisível?
8. **Entrega** com nota de calibração (gatilho usado + framework + objeção principal tratada).

---

## 2.5. Discovery de contexto — protocolo obrigatório

Herda integralmente as 4 perguntas da humanize §2.5 (canal, emissor, leitor, objetivo). Persuade adiciona 3 perguntas específicas obrigatórias antes de aplicar gatilho.

### 🔴 Camada 1, sempre perguntar se faltar

**1. Canal / formato** — herdado de humanize. Ver opções lá.

**2. Emissor** — herdado de humanize. Define qual voz aplicar (Valter / NodusHub / Olympus / Brenda / cliente).

**3. Leitor + estágio de consciência (Schwartz) + temperatura**

Persuade exige granularidade maior que humanize. Pra aplicar gatilho certo, preciso saber em que estado mental o leitor está.

Estágio de consciência (Eugene Schwartz):
- **Unaware** — não sabe que tem o problema. Gatilho: pattern interrupt + diagnóstico. Ex: dentista achando que "convênio resolve".
- **Problem-aware** — sabe do problema, não sabe da solução. Gatilho: amplificação de dor + nomear o problema. Ex: dentista que sente agenda buraca mas acha que "é inverno".
- **Solution-aware** — conhece soluções genéricas, não a sua. Gatilho: comparação + diferencial mecânico. Ex: dentista sabe que existe "agência odonto" mas não Olympus.
- **Product-aware** — conhece você, ainda não comprou. Gatilho: tratamento de objeção + risk reversal + escassez real. Ex: dentista que recebeu proposta semana passada.
- **Most-aware** — quase fechando. Gatilho: urgência específica + CTA baixo atrito. Ex: dentista pediu contrato.

Temperatura:
- **Frio** — primeira vez ouvindo. Gatilho aceito: curiosity gap, pattern interrupt, prova social forte. NÃO aceita: urgência (parece scam).
- **Morno** — viu 2-3 conteúdos. Gatilho: autoridade demonstrada, identity, comunidade.
- **Quente** — interagiu, pediu info. Gatilho: escassez real, garantia, próximo passo.
- **Cliente atual** — Gatilho: reciprocidade, endowment effect, comunidade.

**4. Objetivo específico** — não basta "vender". Pergunta exata: captar opt-in / qualificar / tratar objeção X / ancorar preço / fechar quente / reativar dormido / vender upsell?

### 🟡 Camada 2, perguntar se peça grande

**5. Prova disponível.** O que existe HOJE pra usar?

- Case nominado com número (Brenda CPL R$15,96)
- Print de conta real
- Depoimento gravado ou escrito
- Contrato fechado / cliente atual
- Resultado próprio (own-account proof)
- Nada ainda — produto pré-PMF, build-in-public

Sem essa pergunta, persuade tende a fabricar prova. INVIOLÁVEL §6.

**6. Antagonista nomeado.** Vai atacar quem?

- Concorrente direto (agência de marketing odonto)
- Abordagem comum (Google Meu Negócio + indicação boca a boca)
- Crença do leitor (acha que "convênio resolve")
- Categoria inteira (gurus de tráfego)
- Nenhum — só apresenta

Inimigo nomeado ativa tribalismo (Neuromarketing §3.5). Sem antagonista, gatilho identity fica fraco.

**7. Oferta estruturada.** O que já está definido?

- Preço final
- Garantia condicional (qual gatilho de acionamento?)
- Escassez real (quantas vagas/quando fecha?)
- Bonus stack (o que entra além do core?)
- Risk reversal (devolução? trial? sem fidelidade?)
- Próximo passo concreto (link Cakto, formulário, ligação Calendly)

Se não tem oferta definida, persuade vira teoria. Ver §6.

### 🟢 Camada 3, perguntar só se crítico

- Estágio de funil (TOFU lead frio / MOFU morno / BOFU quente)
- Big idea / âncora narrativa já decidida ou vou caçar
- Restrições de plataforma (Meta proíbe before-after médico, etc)
- Tempo até a peça ir ao ar (urgência interna define se vale A/B)

**Formato da pergunta:** mesma regra da humanize. AskUserQuestion até 4/rodada, opções com exemplo concreto, opção recomendada quando óbvio.

**Quando pular discovery:** mesma regra da humanize. Edição de copy existente, pedido específico completo, ajuste trivial.

---

## 3. Gatilhos canônicos — catálogo operacional

Cada gatilho vem com: **nome + mecanismo neural em 1 linha · aplicação CERTA (humano) · aplicação ERRADA (cringe IA) · exemplo BR NodusHub**. Para mecanismo profundo, ver Neuromarketing §referenciado.

### 3.1 Os 7 Cialdini clássicos

**Reciprocidade** — cérebro registra dívida quando recebe valor antes de pagar (Neuromarketing §2.1).
- CERTO: dar Mapa FOCO R$0 com diagnóstico real dos 4 buracos do funil odonto.
- ERRADO: "baixe nosso ebook gratuito sobre marketing digital".
- Olympus: "Te mando o Mapa FOCO. Lê em 12 min. Se fizer sentido, a gente conversa."

**Compromisso e consistência** — cérebro busca coerência com decisões públicas anteriores (§2.2).
- CERTO: pedir micro-sim antes do sim grande. "Faz sentido pra você?" → "Top, te mando proposta."
- ERRADO: "comprometa-se com sua jornada de transformação".
- NodusHub: pitch começa com "você concorda que tá perdendo paciente particular pro convênio?" → resposta sim ativa consistência pra resto.

**Prova social** — cérebro toma atalho pelo que outros como ele fizeram (§2.3 + §1.9).
- CERTO: "Caroline, Brenda Studio Renova Mandaguaçu, 18 conversas em 30 dias, R$15,96 cada, conta act_459091013859000."
- ERRADO: "Mais de 1.000 clientes satisfeitos!" / "Resultados comprovados".
- Olympus: nome do dentista + cidade + número específico de paciente novo. Sem nome = sem prova.

**Afeição / likeability** — gostamos de quem se parece com a gente (§2.4).
- CERTO: Valter mineiro de Maringá fala com dentista de interior PR. Sotaque, gírias regionais, contexto local.
- ERRADO: "somos apaixonados pelo que fazemos".
- Brenda: voz feminina próxima, ASMR, "minha cliente Daniela veio quarta".

**Autoridade** — cérebro economiza energia delegando pra especialista (§2.5).
- CERTO: print da conta act_459091013859000 mostrando R$30/dia rodando. Foto do contrato. Vídeo do dashboard real.
- ERRADO: "especialista certificado em tráfego pago" / "anos de experiência" / "expertise comprovada".
- Valter: "Não sou guru. Construí o sistema que roda na minha esposa. Conta tá aqui ó."

**Escassez (real, nunca fabricada)** — perda potencial > ganho potencial (§2.6 + §1.3).
- CERTO: "4 vagas Founding Member. Quando fechar a 4ª, lista fecha. Estamos na 2ª." (auditável)
- ERRADO: "Últimas vagas!" eterno na LP.
- Olympus: número de vagas = número de slots de operação real do Valter (5 dentistas até 15/06).

**Unidade (Pre-Suasion 2016)** — pertencimento de identidade > simples afeição (§2.7).
- CERTO: "Pra dentista que cansou de agência cobrar R$5-15k e entregar planilha bonita." Identifica tribo.
- ERRADO: "Para quem busca excelência" (genérico, sem tribo).
- NodusHub: "Founders B2B que vendem por relacionamento e querem CRM que não atrapalha."

### 3.2 Gatilhos avançados (Neuromarketing §3)

**Especificidade / números quebrados** — cérebro confia mais em R$15,96 que R$16 (§3.1).
- CERTO: "CPL R$15,96 últimos 30d em Mandaguaçu PR."
- ERRADO: "Aproximadamente R$15-20 por lead."

**Novidade** — cérebro registra como ameaça/oportunidade, dispara dopamina (§3.2).
- CERTO: "Stack que junta tráfego + Iris (atendente IA) + CRM num produto só. Ninguém faz isso por R$1.797."
- ERRADO: "Solução inovadora e disruptiva."

**Concretude sensorial** — palavra concreta vence palavra abstrata (§3.3).
- CERTO: "Terça 14h, cadeira vazia, recepcionista olhando o celular."
- ERRADO: "Horário comercial com baixa demanda."

**Contraste** — cérebro precisa de referência (§3.4 + §1.7).
- CERTO: "Agência: R$5-15k/mês + planilha. Olympus: R$1.797 + sistema rodando."
- ERRADO: "Investimento acessível com alto retorno."

**Tribalismo / inimigo nomeado** — in-group vs out-group ativa identidade (§3.5).
- CERTO: "Pra dentista que sabe que convênio não paga conta de luz."
- ERRADO: "Para todos os profissionais da saúde."

**Curiosity gap (Brian Clark)** — abre loop mental que cérebro PRECISA fechar (§3.6).
- CERTO: "Os 4 buracos do funil odontológico que toda agência ignora."
- ERRADO: "Descubra o segredo do sucesso."

**Comparação implícita** — sem âncora, leitor não tem referência (§3.7 + §1.7).
- CERTO: âncora de preço (agência R$5-15k), âncora temporal (30 dias vs 6 meses), âncora de esforço (você sozinho vs sistema).
- ERRADO: oferta solta sem referência.

### 3.3 Loss aversion / Endowment (§1.3 + §1.8)

**Loss aversion** — perder dói 2,5× mais que ganhar.
- CERTO: "Você perdeu 8 pacientes particulares em maio que foram pro convênio. R$24 mil de receita."
- ERRADO: "Ganhe mais pacientes!"

**Endowment effect** — sentir que já tem.
- CERTO: trial 7 dias do Olympus. "Sua conta já está rodando. Cancela quando quiser."
- ERRADO: "Compre agora e ganhe acesso!"

### 3.4 Future pacing — leitor se vê no estado pós-compra

- CERTO (específico): "Quarta que vem, agenda lotada de paciente particular, recepcionista pedindo encaixe."
- ERRADO (genérico): "Imagine sua vida transformada."

### 3.5 Identity-based — "isso é coisa de gente como eu"

- CERTO: "Pra dentista que prefere atender 8 pacientes particulares por dia que 20 do convênio."
- ERRADO: "Para você que busca o melhor."

### 3.6 Pattern interrupt — quebra de expectativa pra abrir atenção

- CERTO: abrir post com "Esqueci de ligar pro paciente quarta. Perdi consulta de R$1.200."
- ERRADO: "Você sabia que perder pacientes custa caro?"

### 3.7 Compromise commitment — sim pequeno → sim grande

- CERTO: lead magnet R$0 → tripwire R$37 → core R$1.797 → upsell R$497/mês.
- ERRADO: pular do anúncio direto pra ticket alto sem escada.

> **Princípio meta:** gatilho não substitui produto bom. Se a oferta não resolve o problema do leitor, nenhum gatilho salva. Persuasão amplifica oferta verdadeira, não fabrica venda fake.

---

## 4. Cheat sheet ANTES → DEPOIS de gatilho mal aplicado

Mesma lógica da humanize §4, mas focado em estrutura persuasiva. Se o ANTES aparece, reescreve.

| ANTES (gatilho fabricado / cringe IA) | DEPOIS (gatilho honesto / humano) |
|---|---|
| Resultados incríveis em pouco tempo | Brenda Studio Renova: 18 conversas em 30 dias, R$15,96 por conversa |
| Limitado! Últimas vagas! | 4 vagas Founding Member com contrato + CNPJ. Quando fechar a 4ª, lista fecha. Estamos na 2ª. |
| Especialista certificado em marketing odonto | Construí o sistema que roda na minha esposa. Conta act_459091013859000, R$30/dia. |
| Garantia de satisfação total | 3 primeiros meses sem fidelidade. Se a campanha não rodar, cancela sem multa, por escrito. |
| Mais de 1.000 clientes satisfeitos | Caroline (Brenda Studio Renova, Mandaguaçu PR) e Daniela (Estética & Cia, Maringá PR). |
| Aproveite essa oportunidade única | Inscrição fecha sexta 23/05 às 23h59. Próxima turma em outubro. |
| Não perca tempo, garanta já o seu | Topa quarta 14h pra eu te mostrar a conta rodando? |
| Resultados que falam por si | R$241,36 gastos, 7 conversas iniciadas, 0 handoff Iris em 7d. Esse é o número real. |
| Solução completa e inovadora | Tráfego + atendente IA + CRM num produto só. Ninguém vende stack assim por R$1.797. |
| Investimento acessível | R$1.797 setup + R$497/mês. Agência cobra R$5-15k/mês só pela parte do tráfego. |
| Imagine se você pudesse ter agenda cheia | Quarta 9h, agenda de cirurgia bloqueada três semanas à frente. |
| Você merece o melhor | (apaga, mostra o que o produto resolve) |
| Resultados comprovados | Print da conta + contrato anexo. |
| Transformação garantida | (apaga, escreve a garantia condicional específica) |
| Saia do óbvio | (apaga) |
| Vá para o próximo nível | (apaga, descreve o que muda concretamente) |
| Descubra o segredo de | Os 4 buracos do funil odontológico que ninguém te conta |
| E se eu te dissesse que... | A maioria dos dentistas perde 8 pacientes/mês pro convênio. Olha como. |
| Experiência única e exclusiva | Sistema que roda só pra 5 dentistas até 15/06. Founding Member com CNPJ. |
| Atendimento personalizado | Você fala direto comigo no WhatsApp, sem suporte tier 1. |
| Para quem busca excelência | Pra dentista que cansou de agência cobrar R$5-15k e entregar planilha bonita. |
| Faça parte dessa transformação | Topa testar 30 dias e ver a conta rodando? |
| Inscreva-se já! | Te mando o link da Cakto. R$1.797 parcelado em 12×. |
| Garantimos seu sucesso | 90 dias sem fidelidade. Cancela por mensagem, sem multa. |
| Por tempo limitado | Encerra sexta 23/05 23h59 (UTC-3). |
| Compre agora e ganhe... | Founding Member ganha auditoria mensal + acesso direto comigo. |
| Resultados extraordinários | (apaga, mostra o número) |
| Eleve seu negócio a outro patamar | Tira do lugar onde tá travado: 12 atendimentos/dia particulares. |
| Você precisa disso | (apaga, escreve por que importa pra ELE específico) |
| Oferta imperdível | (apaga, mostra a comparação de preço real) |
| Decida agora, transforme amanhã | Topa fechar quarta? Setup começa quinta. |
| Última chance | Sexta às 23h59. Sem prorrogação. |

---

## 5. Frameworks de copy persuasiva (humanizados)

Cada framework: **quando usar · estrutura · 1 exemplo aplicado**. Pra teoria completa ver `Copywriting-Humano-Metodo-Completo-2026.md` + Neuromarketing-Persuasao §5.

### 5.1 PAS — Problem, Agitate, Solution

- **Quando:** copy curta (anúncio Meta, email curto, post), lead problem-aware.
- **Estrutura:** P (1-2 frases nomeando o problema concreto) → A (1-3 frases mostrando o custo do problema) → S (1 frase apresentando a solução com prova).
- **Olympus exemplo:** "Você perdeu 8 pacientes particulares em maio pro convênio. (P) São R$24 mil de receita que foi pro pé do colega que tem 3 cadeiras a mais. (A) Olympus instala tráfego + atendente IA + CRM em 7 dias. Mandaguaçu PR roda 18 conversas/mês por R$15,96 cada. (S)"

### 5.2 AIDA — Attention, Interest, Desire, Action

- **Quando:** anúncio com espaço (primary text Meta longo), email médio, vídeo curto.
- **Estrutura:** A (hook que quebra padrão) → I (contexto + insight novo) → D (future pacing + prova) → A (CTA específico).
- Mais usado em ad creative + email cold.

### 5.3 BAB — Before, After, Bridge

- **Quando:** LP de tripwire, post de carrossel, ad com vídeo.
- **Estrutura:** Before (estado atual com dor sensorial) → After (estado desejado com cena específica) → Bridge (o mecanismo que leva um ao outro).
- **Mapa FOCO exemplo:** Before — "Agenda buraca, recepcionista jogando paciência no celular." After — "Agenda lotada de particular, encaixe pedido às quartas." Bridge — "PDF de 12 páginas com os 4 buracos exatos do funil odonto. R$0."

### 5.4 PASTOR (Ray Edwards) — Problem, Amplify, Story+Solution, Testimony, Offer, Response

- **Quando:** VSL, carta de venda longa, página de oferta densa.
- **Estrutura:** P (nomeia) → A (amplifica custo emocional + financeiro) → S+S (história específica + mecanismo) → T (3-5 depoimentos com nome) → O (oferta com stack de valor + garantia) → R (CTA + escassez real).
- Ver §5 completo em Neuromarketing-Persuasao-2026.

### 5.5 StoryBrand SB7 (Donald Miller)

- **Quando:** LP institucional, deck de proposta, vídeo institucional.
- **Estrutura:** Hero (cliente, não você) tem Problema → encontra Guide (você, com autoridade demonstrada + empatia) → recebe Plano (3 passos concretos) → é chamado pra Ação → evita Falha → vive Sucesso.
- **NodusHub exemplo:** Hero = dentista cético. Problema = perde paciente pro convênio. Guide = Valter (mostra Brenda como prova). Plano = (1) instala stack 7d, (2) Iris atende 24/7, (3) tráfego roda R$30/d. Ação = "topa quarta 14h?". Falha = continuar perdendo R$24k/mês. Sucesso = agenda lotada de particular.

### 5.6 4Ps (Promise, Picture, Proof, Push)

- **Quando:** ad creative, headline LP, hero acima da dobra.
- **Estrutura:** Promise (1 linha promessa específica) → Picture (1 cena visual) → Proof (1 número/nome) → Push (1 CTA).
- Hooks-copy-br entrega o Promise/Picture; persuade entrega Proof/Push.

### 5.7 Sabri Suby — The Godfather Strategy (oferta que não dá pra recusar)

- **Quando:** lançamento, oferta de tripwire pra core, reativação.
- **Estrutura:** Oferta tão boa que parece estúpido recusar = (Big Promise específica) + (Stack de valor que vale 5-10× o preço) + (Garantia que tira todo risco) + (Escassez real) + (Razão crível pro preço baixo).
- **Olympus Founding Member exemplo:** R$1.797 setup com sistema que agência cobra R$5-15k/mês + Iris incluída + CRM incluído + 3 meses sem fidelidade + 4 vagas (porque eu só atendo 5 clientes até 15/06) + auditoria mensal direto comigo.

> **Regra de escolha:** copy curta = PAS ou 4Ps. Copy média = AIDA ou BAB. Copy longa = PASTOR ou SB7. Oferta forte = Sabri Godfather por cima de qualquer framework.

---

## 6. Estrutura de oferta irresistível (Hormozi BR)

Referência base: Alex Hormozi, *$100M Offers*, adaptado pra NodusHub. Detalhes em Neuromarketing §10 + Copywriting-Humano §oferta.

### 6.1 Equação de valor (Hormozi)

Valor percebido = (Dream Outcome × Perceived Likelihood) / (Time Delay × Effort & Sacrifice)

Operacional:
- **Dream Outcome:** definir em 1 frase concreta (NÃO "ganhar mais", SIM "agenda lotada de paciente particular em 30 dias").
- **Perceived Likelihood:** prova social específica + garantia condicional + mecanismo demonstrado.
- **Time Delay:** quanto tempo até o resultado? Encurta se possível. Olympus = 7d setup + primeira semana já roda ads.
- **Effort & Sacrifice:** o que o cliente precisa fazer? Reduz a quase zero. Olympus = "nada, eu instalo. Você só responde paciente no WhatsApp."

### 6.2 Stack de valor com bonus

Lista item por item com valor declarado, totaliza, mostra preço final, gera contraste.

**Olympus Founding Member exemplo:**
- Sistema de tráfego configurado (vale R$3.000)
- Iris atendente IA 24/7 (vale R$1.500/mês)
- CRM cliente (vale R$497/mês)
- Auditoria mensal direto comigo (vale R$1.000/mês)
- 3 meses sem fidelidade (vale priceless)
- Acesso ao grupo de Founding Members (vale R$500/mês)

Total declarado: R$6.497 + recorrentes.
Preço real: R$1.797 setup + R$497/mês.
Razão crível: "Eu só atendo 5 clientes até 15/06. Founding Member trava o preço pra sempre."

### 6.3 Garantia condicional vs incondicional

- **Incondicional** (devolução total se não gostar) — alto risco pra você, alta conversão se produto entrega.
- **Condicional** (garantia mediante critério objetivo) — médio risco, blinda contra abusador.
- **Olympus:** "3 primeiros meses sem fidelidade. Se a campanha não roda primeiros 30 dias (zero conversa iniciada), te devolvo setup. Por escrito no contrato."

### 6.4 Risk reversal — quem assume o risco

Padrão SaaS / agência: cliente assume risco. Olympus inverte: você assume risco operacional, cliente paga só se rodar.

Aplicação:
- Trial 7 dias (cliente prova antes de pagar full)
- Sem fidelidade nos primeiros 90d
- Garantia condicional escrita
- Reembolso pro-rata se cancelar

### 6.5 Aplicação Mapa FOCO R$37 (tripwire)

- Dream Outcome: clareza dos 4 buracos do seu funil odonto.
- Perceived Likelihood: 12 páginas PDF + auditoria gravada + bonus de bate-papo 30min comigo.
- Time Delay: lê em 12 min, aplica em 1 semana.
- Effort: zero, é PDF + áudio.
- Stack: PDF + áudio + 30min comigo + acesso ao grupo Telegram (R$37 total, valor declarado R$500+).
- Garantia: 7 dias devolução por mensagem.

---

## 7. Tratamento de objeção

Toda objeção tem 2 camadas: **lógica** (argumento racional) e **medo** (custo emocional de errar). Tratar só lógica = cliente concorda e não compra. Tratar só medo = cliente compra e arrepende.

### 7.1 4 categorias universais de objeção

1. **Preço** — "tá caro" / "não cabe agora". Medo: errar de novo, perder dinheiro.
2. **Tempo** — "não tenho tempo agora" / "quem sabe mês que vem". Medo: começar e não conseguir manter.
3. **Confiança** — "como sei que funciona" / "já tentei agência". Medo: ser enganado de novo.
4. **Autoridade própria** — "preciso conversar com sócio" / "vou pensar". Medo: tomar decisão errada sozinho.

### 7.2 Pre-emption vs tratamento direto

- **Pre-emption:** trata objeção ANTES do leitor formular. Usado em VSL e LP longa.
- **Tratamento direto:** responde quando objeção já foi colocada (DM, ligação, follow-up).

Pre-emption funciona melhor com leitor mais sofisticado (cético experiente). Tratamento direto funciona com lead morno-quente.

### 7.3 8 objeções dentista odonto (mapeadas em vault)

| Objeção | Camada lógica | Camada medo | Gatilho a usar |
|---|---|---|---|
| "Já tentei agência e não funcionou" | Diferencial mecânico (stack vs serviço) | Medo de perder R$5-15k de novo | Prova específica (Brenda) + garantia condicional |
| "R$1.797 tá caro" | Comparação com agência R$5-15k/mês | Medo de gastar e não voltar | Anchoring + risk reversal |
| "Não tenho paciente pra atender mais" | Diagnóstico de capacidade real (cadeira ociosa) | Medo de virar fábrica | Prova de Brenda (qualifica, não inunda) |
| "Convênio já paga conta" | Matemática R$/hora particular vs convênio | Medo de perder convênio existente | Loss aversion (8 pacientes perdidos) |
| "Vou pensar / falar com sócio" | Custo de espera (cada mês = R$24k perdido) | Medo de decisão isolada | Future pacing + próximo passo baixo atrito |
| "Não confio em marketing digital" | Demonstração ao vivo da conta | Medo de ser enganado | Autoridade demonstrada (print conta act_) |
| "Minha agenda já tá cheia" | Auditoria: % particular vs convênio | Medo de mexer no que funciona | Reframing (qualidade vs quantidade) |
| "Tenho dúvida sobre LGPD/CFO" | Compliance explicado (Iris não diagnóstica) | Medo de processo | Autoridade técnica + contrato anexo |

### 7.4 6 objeções founder B2B (NodusHub institucional)

| Objeção | Tratamento |
|---|---|
| "Já tenho RD/HubSpot" | Stack vs ferramenta. RD é CRM, NodusHub é sistema completo. |
| "Meu time já faz isso" | Mostrar custo do time alocado vs preço NodusHub. |
| "Marketing não é prioridade agora" | Reframe: aquisição não é marketing, é receita. |
| "Vou esperar próximo trimestre" | Loss aversion: meses de fila perdidos. |
| "Preciso de mais cases B2B" | Adjacência: Brenda funciona porque sistema, não nicho. |
| "Não tenho budget de tráfego" | R$30/dia. Anchoring contra CAC orgânico do time. |

### 7.5 Rebrandar vs atacar objeção

- **Rebrandar:** quando a objeção é sintoma de outro problema. "Não tenho tempo" geralmente é "não confio que vai funcionar". Responde o subterrâneo.
- **Atacar direto:** quando a objeção é técnica e tem resposta clara. "Funciona com LGPD?" → sim, contrato anexo, eis o trecho.

> Princípio: pergunta antes de responder. "Quando você diz que tá caro, é caro em relação a quê?" abre a objeção real.

---

## 8. Auto-policia operacional

Antes de devolver QUALQUER copy persuasiva, marca cada item. Falhou um → reescreve antes de mandar.

- [ ] Toda promessa tem prova específica (número, nome, print) — INVIOLÁVEL §6.
- [ ] Toda escassez é REAL (vagas auditáveis, data específica) — §1.
- [ ] Toda urgência tem data concreta — §2.
- [ ] Todo big number tem nome de cliente ou conta auditável — §6.
- [ ] Autoridade demonstrada (não declarada) — §4.
- [ ] CTA é específico (não "saiba mais") — §10.
- [ ] Pelo menos uma objeção principal foi tratada (lógica + medo) — §9.
- [ ] Gatilho não virou cringe (passou pelo teste do bar da humanize) — crossover §9.
- [ ] Estágio de consciência do leitor combina com gatilho usado.
- [ ] Anchoring tem referência real (preço de mercado, não inventado) — §7.
- [ ] Storytelling tem nome, hora, local específicos — §8.
- [ ] Crossover com humanize: zero travessão, zero banword, voz do emissor mantida.
- [ ] Garantia (se existe) tem gatilho objetivo de acionamento.
- [ ] Pre-suasion: leitor preparado mentalmente ANTES da oferta?
- [ ] Framework escolhido (PAS/AIDA/BAB/PASTOR/SB7/4Ps/Sabri) está claro na estrutura.
- [ ] Se peça é longa: releu inteira em voz alta mentalmente, gatilho ficou invisível.

Entrega com nota:
```
Copy persuasiva entregue. 
Framework: [PAS / AIDA / BAB / PASTOR / SB7 / 4Ps / Sabri Godfather]
Gatilho principal: [reciprocidade / autoridade / escassez / prova social / loss aversion / curiosity gap / etc]
Objeção tratada: [qual das 4 categorias]
Estágio do leitor: [Unaware / Problem / Solution / Product / Most-aware] × [Frio / Morno / Quente / Cliente]
Calibração herdada humanize: [canal · emissor · leitor]
```

---

## 9. Crossover com humanize-copy-br e hooks-copy-br

As três skills trabalham em camadas. Confundir camada = copy ruim.

| Camada | Skill | Função | Quando entra |
|---|---|---|---|
| 1. Porta | `hooks-copy-br` | Atenção nos primeiros 2 segundos | Hook do anúncio, primeira linha do email, capa do carrossel |
| 2. Motor | `persuade-copy-br` | Estrutura de convencimento | Corpo do anúncio, sequência da LP, tratamento de objeção, oferta |
| 3. Acabamento | `humanize-copy-br` | Voz humana sem cara de IA | Toda palavra escrita, sempre |

**Ordem operacional:**
1. Hook abre (hooks-copy-br entrega gancho)
2. Persuade convence (esta skill aplica gatilho + framework + oferta)
3. Humanize policia voz (rede de segurança contra IA-cringe)

**Regra anti-conflito:** se gatilho de persuade precisar usar palavra da blacklist humanize, REESCREVE o gatilho. Humanize sempre vence em conflito de palavra/expressão. Persuade vence em conflito de ESTRUTURA.

**Princípio mestre:** gatilho é arquitetura invisível. Voz é acabamento sentido. Se o leitor ADMIRA o gatilho, gatilho falhou. Se o leitor SENTE a voz e AGE, conjunto ganhou.

---

## 10. Calibração por emissor

Cada emissor tem leverage de persuasão diferente. Mesmo gatilho aplicado em emissor errado vira cringe.

### Valter pessoa (@valterjuniorsilv)

- **Leverage natural:** vulnerabilidade técnica como autoridade. "Construí com minhas mãos, conta tá aqui."
- **Gatilhos fortes:** autoridade demonstrada, transparência (perda + acerto), identity ("dentista que não acredita em guru de tráfego"), tribalismo regional (Maringá, mineiro).
- **Gatilhos fracos:** escassez de produto (Valter pessoa não vende produto, vende encontro/mentoria), urgência (parece estranho na boca dele).
- **Framework preferido:** BAB com história pessoal, PAS curto, story-based.

### NodusHub institucional

- **Leverage natural:** prova de cliente nominal (Brenda, futuros odonto) + sistema replicável.
- **Gatilhos fortes:** prova social específica, anchoring contra agência, autoridade técnica do stack, garantia condicional.
- **Gatilhos fracos:** voz pessoal vulnerável (institucional não chora), urgência genérica.
- **Framework preferido:** SB7 com NodusHub como Guide, PASTOR pra LP longa, 4Ps pra ad.

### Olympus produto

- **Leverage natural:** editorial premium + matemática implacável (R$ por paciente, hora ociosa, perda mensal).
- **Gatilhos fortes:** escassez real (Founding Member 4 vagas), loss aversion (R$24k/mês perdidos), autoridade odonto-específica, comparação com agência.
- **Gatilhos fracos:** humor, voz pessoal, gírias.
- **Framework preferido:** PASTOR pra LP longa, Sabri Godfather pra oferta, PAS pra ad.

### Brenda Studio Renova (cliente nail)

- **Leverage natural:** prova visual (antes-depois), feminino próximo, ASMR, comunidade.
- **Gatilhos fortes:** prova social com foto, identity ("cliente que cuida de si"), reciprocidade (dica grátis no Reel).
- **Gatilhos fracos:** matemática dura, anchoring frio, autoridade técnica.
- **Framework preferido:** BAB visual, AIDA com vídeo, story-based.

### Outro cliente NodusHub

- Aplicar linguagem do nicho.
- Levantar prova específica do nicho ANTES de escrever.
- Pegar 2-3 termos que o leitor usa em conversa real (Voice Mining — ver Copywriting-Humano §Voice Mining).

---

## 11. Sinais forenses de gatilho mal aplicado

Marcadores que denunciam persuasão fabricada / cringe IA. Se 2+ aparecem na peça, reescreve bloco.

1. **Promessa sem prova nominada** — "soluções inovadoras", "resultados que falam por si", "alta performance". Falta nome, número, ou demonstração.
2. **Escassez fabricada / eterna** — "últimas horas" há 6 meses, "vagas limitadas" sem número, "oferta especial" sem data de fim.
3. **Autoridade vazia** — "especialista certificado", "anos de experiência", "expertise comprovada". Não cita FONTE da autoridade.
4. **Urgência inventada** — "não perca essa chance única", "agora ou nunca", "imperdível". Sem âncora temporal real.
5. **Big number anônimo** — "R$50 milhões geridos" (de quem?), "1.000+ clientes" (quais?), "98% de satisfação" (medido como?).
6. **Future pacing genérico** — "imagine sua vida transformada", "transforme seu futuro". Sem cena específica.
7. **Garantia vaga** — "satisfação garantida", "100% garantido". Sem critério objetivo de acionamento.
8. **Anchoring inventado** — "de R$9.997 por R$97" sem evidência de que alguém pagou R$9.997. Preço fictício de mercado.
9. **Curiosity gap sem entrega** — "descubra o segredo" e o segredo é nada / é genérico.
10. **Identity vazia** — "para você que busca o melhor", "para profissionais de sucesso". Sem tribo nomeada com critério.
11. **Pattern interrupt forçado** — abertura chocante sem conexão real com o argumento que vem depois.
12. **Stack de bonus inflado** — "vale R$10.000" em bonus que ninguém venderia avulso. Anchoring desonesto.

Bônus (não conta no 2+ mas observa):
- Depoimento sem nome completo ou foto → §3 prova social
- "Testado e aprovado" sem fonte → §11 banword
- "Método exclusivo" sem mecanismo descrito → §3.2 novidade fake
- Comparação contra "concorrente genérico" sem nomear → §3.5 tribalismo

---

## 12. Quando NÃO usar persuade-copy-br

- **Post de bastidor sem oferta.** Ex: Valter postando "ontem fechei contrato com o terceiro dentista". Conta a história, ponto. Forçar gatilho aqui mata autenticidade.
- **Atendimento técnico.** Iris respondendo "tem horário sexta 14h?" não vende, agenda.
- **Comunicação interna NodusHub.** Time interno não precisa de gatilho mental.
- **Resposta genérica a comentário.** "Top!" "Valeu!" sem agenda comercial.
- **Conteúdo educativo puro.** Post explicando como funciona Meta Ads Library. Autoridade vem da demonstração, não da venda.
- **Citação direta / depoimento.** Não edita a fala do cliente pra "ficar mais persuasiva". Trai voz real.
- **Texto técnico de contrato / compliance.** Segue template legal.
- **Pergunta direta operacional.** "Que horas é a call?" responde direto, não vira pitch.

> Regra: se a peça NÃO pede ação específica do leitor, persuade não entra. Humanize sempre entra.

---

## 13. Referências profundas — quando ler o quê

Esta skill é instrução operacional. Pra teoria/exemplo expandido, consultar:

**Doc-mãe principal:**
- **`/Users/valtersilva/Documents/Obsidian Vault/Conceitos/Neuromarketing-Persuasao-2026.md`** (1461 linhas, 13 capítulos). Capítulo 1 (§1.1-1.10) — fundamentos neurais (Sistema 1/2, loss aversion, dopamine, mirror neurons, anchoring, endowment, social proof neural, reciprocity neural). Capítulo 2 (§2.1-2.7) — 7 Cialdini com aplicação BR. Capítulo 3 (§3.1-3.7) — gatilhos avançados (especificidade, novidade, concretude, contraste, tribalismo, curiosity gap, comparação). Capítulo 4 — escassez e urgência aprofundadas. Capítulo 5 — autoridade demonstrada vs declarada. Capítulo 6 — framing e narrativa. Capítulo 7 — storytelling persuasivo. Capítulo 8 — objection handling neural. Capítulo 9 — CTAs (anatomia + casos). Capítulo 10 — oferta irresistível (Hormozi BR). Capítulo 11 — aplicação NodusHub/Olympus. Capítulo 12 — crossover com humanize. Capítulo 13 — métricas de validação.
  - **Leia capítulos 1-2 quando:** primeira aplicação de gatilho em peça nova, suspeita de gatilho mal calibrado, peça grande (VSL/LP longa).
  - **Leia capítulos 3-7 quando:** caçando gatilho avançado pra peça específica, refinando hook ou estrutura.
  - **Leia capítulos 8-10 quando:** estruturando oferta, tratando objeção complexa, escrevendo CTA crítico.
  - **Leia capítulos 11-13 quando:** aplicação direta NodusHub/Olympus, validação anti-cringe, checklist final.

**Docs complementares (herdados da humanize §9):**
- `Conceitos/Comunicacao-Humana-BR-Anti-IA-2026.md` — taxonomia anti-IA. Leia quando gatilho saiu cringe.
- `Conceitos/Oralidade-BR-Internet-2026.md` — voz BR digital. Leia pra calibrar Reel/TikTok/Stories persuasivo.
- `Conceitos/Copywriting-Humano-Metodo-Completo-2026.md` — 7 copywriters BR + 7 internacionais. Leia pra framework profundo (Voice Mining, Settle, Sabri, Hormozi BR).

**Regra:** abra o capítulo específico quando o caso pede. Não tenta memorizar a enciclopédia.

---

## 14. Skill viva — loop de evolução

**Protocolo de update:**
1. Valter pega gatilho mal aplicado → identifica o padrão exato.
2. Adiciona entrada nova em §4 (cheat sheet) ou §11 (forenses).
3. Se o caso é gatilho novo (não na §3), adiciona ao catálogo + referencia capítulo do doc-mãe.
4. Marca rodapé com versão + data.
5. Se for teoria nova → adiciona ao Neuromarketing-Persuasao-2026.md.

**Antipadrão:** não criar exceções. "Normalmente escassez precisa ser real, mas nesse caso pode fabricar" = regra errada. Skill é dura.

---

## 15. Rodapé — versão e princípio mestre

**Versão:** v1.0 — 2026-05-21 (skill criada)
**Origem:** complementa `humanize-copy-br` v1.2. Pedido do Valter em 2026-05-21: "skill MOTOR de convencimento que aplica gatilhos sobre voz humana, sem confundir com humanize (acabamento) nem com hooks (porta)."

**Skills relacionadas (3 camadas):**
- `hooks-copy-br` (porta de atenção — primeiros 2s)
- `persuade-copy-br` (esta — motor de convencimento)
- `humanize-copy-br` (acabamento — voz BR anti-IA, INVIOLÁVEL)

**Skills secundárias por emissor (mesmas da humanize §7):**
- `tom-valter`, `copy-nodus`, tom Olympus editorial, `marketing-copy`, `imobiliaria-copy-specialist`

**Princípio mestre:**
Persuasão honesta é arquitetura invisível. Se o leitor SENTE o gatilho, o gatilho falhou. Se o leitor age e depois agradece, o conjunto ganhou. Gatilho fabricado vende uma vez e queima a marca. Gatilho real construído com prova, escassez auditável, autoridade demonstrada e objeção tratada vende uma vez, gera caso, gera referência, gera próxima venda. Persuade serve o produto verdadeiro. Se o produto não entrega, nenhum gatilho salva.
