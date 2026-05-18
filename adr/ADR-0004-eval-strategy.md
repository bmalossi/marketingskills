# ADR-0004 — Estratégia de Evals e QA

- **Status:** accepted
- **Data:** 2026-05-18
- **Responsável:** Automab.dev (Bruno)

## Contexto

Skills de IA sem avaliação sistemática acumulam regressão silenciosa: mudam de qualidade sem que ninguém perceba. É preciso definir como avaliar a qualidade dos outputs antes de ir a produção e como manter essa qualidade ao longo do tempo.

## Decisão

Adotar uma estratégia de evals em dois níveis:

### Nível 1 — Rubrica geral (toda skill, todo output)

Arquivo: `evals/rubrica-geral.md`

| Critério | Peso | É crítico? |
|----------|------|-----------|
| Aderência ao contexto | 20% | Sim |
| Naturalidade PT-BR | 15% | Sim |
| Clareza e estrutura | 15% | Não |
| Persuasão comercial | 20% | Sim |
| Utilidade operacional | 20% | Sim |
| Consistência de marca | 10% | Não |

- Score mínimo: 8.0/10 médio
- Critérios críticos: nenhum abaixo de 7.0/10
- Skills que não passam voltam para refinamento antes do go-live

### Nível 2 — Casos de eval por skill (evals/)

Cada skill tem uma pasta em `evals/[nome-da-skill]/` com casos de teste estruturados:
- Input completo e realista
- Output esperado descrito
- Critérios de reprovação automática
- Avaliador designado

### Ciclo de eval

1. Skill escrita em `skills/` → status: `draft`
2. Autoavaliação com rubrica geral
3. Revisão técnica (Automab.dev)
4. Revisão comercial (Rayanne Gama Imóveis)
5. Status muda para `approved` após aprovação em ambas as revisões

## Alternativas consideradas

| Alternativa | Motivo de descarte |
|-------------|-------------------|
| Sem evals formais | Qualidade subjetiva e inconsistente |
| Apenas revisão humana | Lento demais para escala |
| Apenas autoavaliação da IA | Não captura problemas de marca e contexto comercial |

## Consequências

- Nenhuma skill vai a produção sem passar pela rubrica
- A qualidade é mensurável e comparável entre versões
- O ciclo de revisão envolve obrigatoriamente a equipe comercial
- Regressões ficam visíveis quando a skill é atualizada
