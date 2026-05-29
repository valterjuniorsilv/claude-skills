# Contribuindo

## Antes de abrir PR

Skill nova precisa:

1. **Caso de uso real** documentado no top do `SKILL.md`
2. **Triggers explícitos** em `description` (Claude Code roteia por matching de texto na description)
3. **Exemplo antes/depois** se for skill de comportamento (tom, formato, regra)
4. **Override hierárquico declarado** se conflitar com outras skills (quais skills suprime quando ativa)
5. **Regra de desativação clara** (como o usuário desliga)

## Estrutura de pasta

```
categoria/
└── nome-da-skill/
    └── SKILL.md
```

Apenas `SKILL.md`. Sem README extra (a description já é o README).

## Frontmatter obrigatório

```yaml
---
name: nome-skill
description: O que faz · Quando ativar · Triggers PT-BR · Triggers EN · Quando NÃO usar · Override hierárquico
---
```

A description é o que Claude Code lê pra decidir quando invocar. Quanto mais explícita, melhor o routing.

## Idioma

- Skills universais: EN + PT-BR triggers (alcance global)
- Skills `copy-br/`: PT-BR only (são específicas pro mercado brasileiro)
- Skills `claude-code-meta/`: PT-BR + EN se possível

## PR review

Cada PR é revisado por:

1. **Triggers conflitam com skill existente?** Se sim, declarar precedência.
2. **Description tem mais de 12 palavras?** Bom (Claude Code precisa de contexto pra rotear).
3. **Funciona no Claude Code real?** Test em sessão própria antes de abrir PR.
4. **Documenta limitações honestas?** "Funciona em X, falha em Y" é OBRIGATÓRIO.

## Frases que rejeitam o PR

- "Esta skill é incrível" → cortar
- "Você vai amar usar" → cortar
- "Skill perfeita pra todos os casos" → cortar (NUNCA é)
- "Funciona 100% do tempo" → cortar (nunca funciona 100%)

Skills documentadas com humildade técnica são aceitas. Skills com marketing language são rejeitadas.

## Issues

- Bug: passos pra reproduzir + comportamento esperado vs real
- Sugestão: caso de uso real + skill que resolve hoje (ou nenhuma)
- Pergunta: leia o SKILL.md primeiro

## Credits

Skill nova ganha linha no rodapé com link pro autor. Forks/adaptações de skills existentes mantêm crédito original + adicionam o seu.
