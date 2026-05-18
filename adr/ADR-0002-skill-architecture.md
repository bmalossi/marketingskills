# ADR-0002 — Arquitetura de Skills

- **Status:** accepted
- **Data:** 2026-05-18
- **Responsável:** Automab.dev (Bruno)

## Contexto

É preciso definir como as skills serão estruturadas, versionadas e avaliadas para garantir consistência, previsibilidade e qualidade ao longo do projeto.

## Decisão

Adotar a seguinte arquitetura para todas as skills do projeto:

### Estrutura de arquivo

```
skills/
└── [nome-da-skill]/
    ├── SKILL.md         # Definição completa da skill
    └── examples/
        ├── exemplo-01.md
        └── exemplo-02.md
```

### Frontmatter obrigatório

```yaml
---
name: [nome]
version: v0.1
status: draft | review | approved
description: [1 linha]
triggers: [lista de gatilhos de uso]
last_updated: YYYY-MM-DD
---
```

### Blocos obrigatórios do SKILL.md

1. `## Quando usar`
2. `## Inputs obrigatórios`
3. `## Inputs opcionais`
4. `## Framework de execução`
5. `## Formato de saída`
6. `## Anti-padrões`
7. `## Exemplos aprovados`
8. `## Rubrica de avaliação`

### Critério de go-live

- Score médio >= 8.0/10 na rubrica geral
- Nenhum critério crítico abaixo de 7.0/10
- Status: `approved`
- Mínimo 2 exemplos aprovados

## Alternativas consideradas

| Alternativa | Motivo de descarte |
|-------------|-------------------|
| Skills como arquivos JSON | Menos legível para humanos; dificulta edição manual |
| Skills inline no AGENTS.md | Acoplamento excessivo; dificulta manutenção individual |
| Skills sem rubrica de eval | Qualidade não mensurável; regressão invisível |

## Consequências

- Todas as skills seguem o mesmo formato, facilitando manutenção e avaliação
- O agente pode consumir as skills de forma padronizada
- Novos colaboradores conseguem entender e contribuir com facilidade
- A rubrica de evals cria um critério objetivo de qualidade antes do go-live
