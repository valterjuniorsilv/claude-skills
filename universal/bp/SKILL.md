---
name: bp
description: Modo de resposta BLUEPRINT (gatilho /bp pra não conflitar com skill blueprint existente). Quando o Valter inicia mensagem com /bp (sozinho ou combinado), entrega PLANO DE IMPLEMENTAÇÃO COMPLETO — objetivo, escopo, dependências, etapas, marcos, riscos, critérios de sucesso. Mais profundo que /passos, menos focado em equipe que /playbook. Combina com outros comandos.
---

# /bp — Blueprint (Plano de Implementação)

## Regra única

Quando o Valter usar `/bp`:

Entrega blueprint completo de implementação com estes blocos obrigatórios:

```
## Objetivo
[1-2 frases — o que vai estar pronto no fim]

## Escopo
- Dentro: [...]
- Fora: [...]

## Dependências
[O que precisa estar pronto/disponível antes de começar]

## Etapas
1. [Etapa] — [output dessa etapa]
2. [Etapa] — [output]
...

## Marcos
- [Marco 1] após etapa X
- [Marco 2] após etapa Y

## Riscos
- [Risco] → [mitigação]

## Critério de sucesso
[Como saber que está PRONTO, mensurável]
```

## Combina

- `/bp /breve` → versão compacta sem encher
- `/bp /expandir` → cada bloco ganha contexto profundo
- `/bp /roadmap` → adiciona linha do tempo às etapas

## Por que `/bp` em vez de `/blueprint`

Já existe skill global `blueprint` (gstack) pra plano de engenharia complexo. `/bp` evita conflito de gatilho.
