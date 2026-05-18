# ADR-0003 — Modelo de Contexto Mestre

- **Status:** accepted
- **Data:** 2026-05-18
- **Responsável:** Automab.dev (Bruno)

## Contexto

O repositório original usa uma skill chamada `product-marketing-context` como fonte única de verdade do negócio. Todas as outras skills referenciam esse contexto antes de executar qualquer tarefa. É preciso definir como adaptar esse modelo para o contexto imobiliário da Rayanne Gama Imóveis.

## Decisão

Criar um arquivo `context/product-marketing-context-rayanne-ptbr.md` como fonte única de verdade, com as seguintes seções obrigatórias:

1. `## negócio` — descrição, fundação, regiões, diferenciais
2. `## ICP` — perfil do cliente ideal
3. `## segmentos` — subpersonas por objetivo
4. `## oferta` — tipos de imóvel, faixas de valor, regiões
5. `## diferenciais` — o que separa a Rayanne Gama dos concorrentes
6. `## objeções` — por persona
7. `## linguagem` — tom, vocabulário, bom × ruim
8. `## funil` — etapas, eventos, tempo médio
9. `## SEO local` — cidades, bairros, intenções de busca
10. `## canais` — onde o público está e qual o papel de cada canal
11. `## métricas` — KPIs e metas por canal
12. `## prova social` — depoimentos, dados, cases

Arquivos de persona ficam em `context/personas/` e são referenciados pelo contexto mestre.

## Alternativas consideradas

| Alternativa | Motivo de descarte |
|-------------|-------------------|
| Contexto inline em cada SKILL.md | Duplicação e inconsistência |
| Contexto em JSON | Menos legível; dificulta edição e revisão pela equipe comercial |
| Sem documento de contexto | Skills ficam genéricas e incoerentes entre si |

## Consequências

- O AGENTS.md instrui o agente a sempre ler o contexto mestre antes de qualquer tarefa
- Mudanças no negócio precisam ser atualizadas em um único lugar
- Personas ficam em arquivos separados para facilitar atualização independente
- O contexto mestre é o único documento que exige aprovação obrigatória da Rayanne Gama Imóveis antes de qualquer skill ir para produção
