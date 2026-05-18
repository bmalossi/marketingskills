# ADR-0001 — Estratégia de Fork do marketingskills

- **Status:** accepted
- **Data:** 2026-05-18
- **Responsável:** Automab.dev (Bruno)

## Contexto

O repositório `coreyhaines31/marketingskills` é uma coleção open-source (MIT) de ~40 skills de marketing para agentes de IA, cobrindo CRO, copywriting, SEO, analytics e growth. As skills são arquivos Markdown modulares com frontmatter YAML, projetadas para funcionar com Claude Code e outros agentes compatíveis com o padrão de skills.

A Rayanne Gama Imóveis precisa de um agente de IA especializado em marketing imobiliário PT-BR. O repositório original foi construído com foco em SaaS/produto digital em inglês, mas seus frameworks e estrutura são reutilizáveis.

## Decisão

Fazer um **fork derivado** do repositório original, reescrevendo o conteúdo das skills mais relevantes para o contexto imobiliário PT-BR, mantendo a arquitetura de SKILL.md e AGENTS.md do projeto original.

Não será feita tradução direta. Cada skill será reescrita com:
- Vocabulário e tom imobiliário PT-BR
- Exemplos, métricas e CTAs adequados ao funil de imobiliária
- Contexto mestre específico da Rayanne Gama Imóveis como fonte de verdade

## Alternativas consideradas

| Alternativa | Motivo de descarte |
|-------------|-------------------|
| Criar do zero | Retrabalho desnecessário; o repositório original tem frameworks sólidos |
| Tradução direta | Insuficiente; o contexto SaaS não se mapeia diretamente para imobiliário |
| Usar o original sem modificação | Não tem PT-BR, contexto imobiliário nem integração com o funil da imobiliária |

## Consequências

- O projeto fica independente do upstream (sem sync com o original)
- Mudanças no original não serão incorporadas automaticamente
- A licença MIT permite uso comercial e derivação sem restrições
- Skills do original poderão ser incorporadas ao fork sob demanda, conforme necessidade
