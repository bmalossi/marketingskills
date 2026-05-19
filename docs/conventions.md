# Convenções do Projeto

## Nomenclatura de Pastas e Arquivos

- Sempre em `kebab-case` e minúsculas
- Sem espaços, sem acentos nos nomes de arquivo
- Sufixo `-ptbr` obrigatório em arquivos com conteúdo em português
- Sufixo `-imobiliario` obrigatório em skills derivadas do fork

## Estrutura de Pastas (skills/)

Skills do fork original que não são imobiliárias ficam em `skills/archive/`.
Consulte [`adr/ADR-0005-archiving-generic-skills.md`](../adr/ADR-0005-archiving-generic-skills.md).

```
skills/
  <nome-da-skill-imobiliario>/   # Skills ativas
    SKILL.md
    evals/
      evals.json                 # Mínimo 3 casos de teste imobiliários
    references/
      <arquivo-de-apoio>.md      # Mínimo 1 arquivo
    examples/                    # Opcional — quando houver exemplos aprovados
  archive/
    <skills-do-fork-original>/   # Skills genéricas, preservadas por histórico
    README.md
```


### Exemplos corretos
```
copywriting-imobiliario-ptbr/SKILL.md
comprador-primeiro-imovel.md
ADR-0003-context-model.md
```

### Exemplos incorretos
```
Copywriting PT-BR.md
skill_imobiliaria.md
adr3.md
```

## Versionamento de Skills

```
v0.x  → rascunho / work in progress (não usar em produção)
v1.0  → aprovado para uso interno (passou pela rubrica de evals)
v1.x  → melhorias incrementais sem mudança de estrutura
v2.0  → reescrita significativa ou mudança de inputs/outputs
```

- Toda skill em produção deve ser >= v1.0
- Mudanças de v1.x não precisam de novo ADR
- Mudanças para v2.0 exigem novo ADR ou atualização do ADR original

## Estrutura obrigatória de SKILL.md

```markdown
---
name: [nome da skill]
version: v0.1
status: draft | review | approved
description: [1 linha]
triggers: [quando o agente deve usar esta skill]
last_updated: YYYY-MM-DD
---

## Quando usar
## Inputs obrigatórios
## Inputs opcionais
## Framework de execução
## Formato de saída
## Anti-padrões
## Exemplos aprovados
## Rubrica de avaliação
```

## Status de Documentos

| Status | Significado |
|--------|------------|
| `draft` | Em construção, não usar |
| `review` | Aguardando revisão comercial ou técnica |
| `approved` | Aprovado para uso em produção |
| `deprecated` | Substituído por versão mais nova |

## Critério de Pronto (Definition of Done)

Veja `docs/definition-of-done.md` para critérios completos por tipo de entregável.

## Idioma

- Todo conteúdo de skill, contexto e exemplo: **PT-BR**
- Nomes de arquivo, variáveis e frontmatter YAML: **inglês técnico**
- ADRs e docs de governança: **PT-BR**

## Commits

Seguir padrão Conventional Commits:
```
feat: adiciona skill copywriting-imobiliario-ptbr v0.1
fix: corrige anti-padrão de CTA em social-content
docs: atualiza contexto mestre com persona investidor
eval: adiciona casos de teste para paid-ads
chore: reorganiza estrutura de pastas de examples/
```
