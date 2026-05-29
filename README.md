# Claude Skills — by Valter Silva

[![CI](https://github.com/valterjuniorsilv/claude-skills/actions/workflows/validate.yml/badge.svg)](https://github.com/valterjuniorsilv/claude-skills/actions) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Release](https://img.shields.io/github/v/release/valterjuniorsilv/claude-skills)](https://github.com/valterjuniorsilv/claude-skills/releases)

> Skills customizadas pro [Claude Code](https://claude.com/claude-code), nascidas dentro da operação real da [NodusHub](https://nodushub.com.br) — uma agência IA-first que constrói stacks de aquisição (tráfego pago + atendente de IA + CRM) pra clínicas no Brasil.
>
> Tudo o que tá aqui é o que eu uso todo dia. Não é teoria, não é "boas práticas" — é o que sobreviveu na produção.

---

## O que tem aqui

13 skills divididas em 3 categorias:

### `universal/` — funciona pra qualquer contexto

| Skill | Função |
|---|---|
| [`raw-truth`](./universal/raw-truth/) | Brutal honesty mode — força avaliação crua, zero bajulação. Override de skills de copy/conselho enquanto ativa. |
| [`brain`](./universal/brain/) | Vault deep-search exaustiva. Pra quando precisa puxar TUDO do Obsidian sobre um tema antes de trabalhar. |
| [`ghost`](./universal/ghost/) | Modo resposta crua — sem intro, sem despedida, só o resultado. |
| [`breve`](./universal/breve/) | Máximo 3-5 linhas. Sem perder precisão, só compactando. |
| [`bp`](./universal/bp/) | Blueprint mode — plano de implementação completo (escopo, dependências, ETA). |

### `copy-br/` — pipeline de copy em PT-BR

Sistema canônico de produção de texto pra mercado brasileiro. Combate ativamente "cara de IA" e aplica neuromarketing sem manipular.

| Skill | Função |
|---|---|
| [`orquestrador`](./copy-br/orquestrador/) | Porta única que aciona o pipeline em cascata. |
| [`humanize-copy-br`](./copy-br/humanize-copy-br/) | Voz humana BR — zero hífen/travessão, gírias autênticas, anti-IA. |
| [`hooks-copy-br`](./copy-br/hooks-copy-br/) | Porta de atenção — gancho que segura scroll. |
| [`persuade-copy-br`](./copy-br/persuade-copy-br/) | Motor de persuasão — gatilhos mentais, neuromarketing, estrutura de oferta. |
| [`roteiro-copy-br`](./copy-br/roteiro-copy-br/) | Fluxo interativo pra Reel/TikTok/Short. NUNCA escreve de cara — pergunta primeiro. |

### `claude-code-meta/` — workflow de sessão

| Skill | Função |
|---|---|
| [`save-vault`](./claude-code-meta/save-vault/) | Extrai conhecimento da conversa e salva no Obsidian Vault. |
| [`boa-noite`](./claude-code-meta/boa-noite/) | Salva contexto de TODAS sessões Claude Code abertas. Encerra o dia. |
| [`bom-dia`](./claude-code-meta/bom-dia/) | Retoma de onde parou na sessão anterior. Pareado com boa-noite. |

---

## Como instalar

### Skill individual

```bash
cd ~/.claude/skills
git clone https://github.com/valterjuniorsilv/claude-skills.git tmp-skills
mv tmp-skills/universal/raw-truth ./
mv tmp-skills/universal/brain ./
rm -rf tmp-skills
```

Reabra o Claude Code. As skills aparecem na lista automaticamente.

### Tudo de uma vez

```bash
cd ~/.claude/skills
git clone https://github.com/valterjuniorsilv/claude-skills.git tmp-skills
cp -r tmp-skills/universal/* ./
cp -r tmp-skills/copy-br/* ./
cp -r tmp-skills/claude-code-meta/* ./
rm -rf tmp-skills
```

### Verificar instalação

```bash
ls ~/.claude/skills/raw-truth
```

Tem que aparecer o `SKILL.md`. Pronto.

---

## Por que essas skills existem

### `raw-truth` — porque LLM bajula
RLHF treinou os modelos pra elogiar. Mesmo com instrução "seja imparcial", o reflexo de validar vaza no subtexto. Esta skill ataca o subtexto, não só a forma. Detalhes em [universal/raw-truth/SKILL.md](./universal/raw-truth/SKILL.md).

### `humanize-copy-br` — porque IA escreve igual IA
Travessão em tudo. "Imagine só." "Isso é o que faz a diferença." Linguagem chapada que treinou o algoritmo pra reduzir alcance. Essa skill bloqueia banwords e força oralidade brasileira real.

### `boa-noite` + `bom-dia` — porque Claude Code esquece
Toda sessão começa do zero. Pra builder que trabalha em 5-10 frentes simultâneas, isso é fricção brutal. Esse par resolve.

---

## Stack que essas skills assumem

Algumas skills (principalmente em `claude-code-meta/`) assumem:

- macOS (paths tipo `~/Documents/Obsidian Vault/`)
- Obsidian como vault de conhecimento
- Claude Code instalado (não a API direta)
- `gh` CLI autenticado (algumas skills usam GitHub)

Se você não usa Obsidian, as skills `brain`, `save-vault`, `boa-noite` e `bom-dia` precisam de adaptação. Os triggers em PT-BR também precisam ser traduzidos se você trabalha em outro idioma.

---

## Personalização

Várias skills têm referência ao meu nome (Valter) e à NodusHub. Pra adaptar pro teu contexto:

```bash
cd ~/.claude/skills
grep -rl "Valter" . | xargs sed -i '' 's/Valter/[SEU_NOME]/g'
grep -rl "NodusHub" . | xargs sed -i '' 's/NodusHub/[SUA_OPERACAO]/g'
```

Faça isso DEPOIS de clonar, não no fork — pra manter sync com updates.

---

## Contribuir

PRs bem-vindos. Antes de abrir:

1. Lê [CONTRIBUTING.md](./CONTRIBUTING.md)
2. Skill nova precisa ter caso de uso real, não teoria
3. Triggers explícitos no `description` (Claude Code roteia por isso)
4. Exemplo antes/depois se for skill de comportamento

---

## Licença

MIT. Usa, modifica, comercializa, vende. Só não tira meu nome dos créditos das skills originais.

---

## Autor

**Valter Silva** · Founder [NodusHub](https://nodushub.com.br) · Maringá, PR · 🇧🇷

- 📸 [@valterjuniorsilv](https://instagram.com/valterjuniorsilv)
- 💼 GitHub [valterjuniorsilv](https://github.com/valterjuniorsilv)
- 🏢 Trabalho na operação real: tráfego pago + bots WhatsApp com Claude + CRM próprio pra clínicas odontológicas e estéticas.

> "Na area, não nas arquibancadas."

---

## Roadmap

- [ ] Sprint 2: agents NodusHub sanitizados (`nodus-agents` repo separado)
- [ ] Sprint 2: template de bot WhatsApp (`claude-whatsapp-template`)
- [ ] Sprint 3: tradução EN das skills PT-BR-only
- [ ] Sprint 3: vídeos curtos demonstrando cada skill em uso real
