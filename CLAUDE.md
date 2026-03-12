# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Maestro Dev is a Claude Code plugin (v1.0.0) by @eusouwillnunes for "A Comunidade dos Últimos". It provides 15 specialized AI agent skills that guide non-technical product managers through the full software development lifecycle — from product definition to production deployment.

This is **not a traditional codebase** — there is no compiled code, build system, or package.json. The project consists entirely of Markdown skill definitions (SKILL.md files) and a plugin manifest.

## Structure

```
.claude-plugin/plugin.json   # Plugin manifest (name, version, author)
skills/                      # 15 agent skill definitions
  <agent-name>/SKILL.md      # Each agent's complete specification
README.md                    # User-facing documentation (pt-BR)
```

### Core Agents (7 conversational — activate on natural language triggers)

| Agent | Directory | Expertise |
|-------|-----------|-----------|
| Produto | `skills/produto/` | MVP definition, Lean Canvas, user stories, MoSCoW prioritization |
| Arquiteto | `skills/arquiteto/` | Stack selection, C4 diagrams, ADRs, Blueprint, CLAUDE.md generation |
| Banco de Dados | `skills/banco-de-dados/` | Schema design, relationships, RLS, migrations |
| Setup | `skills/setup/` | Project initialization, dependencies, env config, security |
| Testes | `skills/testes/` | Test strategy (unit/integration/E2E), security validation |
| Deploy | `skills/deploy/` | Local dev environment, production deployment, rollback |
| Git | `skills/git/` | Commit analysis, branch strategy, version history |

### Command Agents (8 — invoked via `/maestro-dev:<command>`)

`iniciar-projeto`, `commit`, `preview`, `rodar-testes`, `fazer-deploy`, `registrar-melhoria`, `consolidar-melhorias`, `revisao-sistema`

## SKILL.md Anatomy

Every skill file follows this structure:
1. **YAML front matter** — name, description, activation `when` clauses
2. **Identidade** — persona (based on industry authorities), beliefs, principles
3. **Interação** — tone, response format, communication rules
4. **Frameworks** — 3-5 named methodologies with detailed steps
5. **Abordagem de Trabalho** — mandatory rules + scenario workflows
6. **Checklist de Validação** — domain-specific + global validation criteria
7. **Restrições** — hard constraints (what the agent must never do)
8. **Exemplos** — good vs. bad examples and scenario walkthroughs

## Conventions

- **Language**: All content in Portuguese (pt-BR); technical terms in English where standard
- **Writing protocol ("Protocolo de Escrita Natural")**: No superlatives without evidence, no clichés (jornada, mergulhar, desvendar, alavancar), max 1 formal connector per 3 paragraphs, no filler phrases
- **Approval pattern**: Agents always show what they'll do and ask for confirmation before executing
- **Trade-offs**: Every recommendation must include explicit trade-offs
- **Non-technical language**: All user-facing communication in business terms

## Editing Skills

When modifying a SKILL.md file:
- Preserve the YAML front matter format — `when` clauses control automatic activation
- Maintain the established section order (Identidade → Interação → Frameworks → Abordagem → Checklist → Restrições → Exemplos)
- Keep the persona references (Cagan, Fowler, Celko, Beck, etc.) — they define methodology alignment
- Test activation triggers by checking `when` patterns don't conflict across agents

## Plugin Installation (for testing)

```bash
# From GitHub
/plugin install github:eusouwillnunes/maestro-dev

# From local ZIP
/plugin install /path/to/maestro-dev.zip

# Update
/plugin update maestro-dev
```

## Expected Workflow Sequence

Agents are designed to work sequentially, each building on the previous output:

Produto → Arquiteto → Banco de Dados → Setup → (development) → Git → Testes → Deploy
