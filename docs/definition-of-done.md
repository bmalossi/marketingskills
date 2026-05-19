# Definition of Done

## Skill (SKILL.md)

Para uma skill ser considerada pronta para produção (status: `approved`):

- [ ] Todos os blocos obrigatórios preenchidos (ver `conventions.md`)
- [ ] Versão >= v1.0
- [ ] Pasta `evals/` presente com ao menos 3 casos de teste imobiliários em PT-BR
- [ ] Todos os evals refletem cenários da Rayanne Gama Imóveis (sem conteúdo SaaS/genérico)
- [ ] Pasta `references/` presente com ao menos 1 arquivo de material de apoio
- [ ] Conteúdo de references/ consistente com o contexto mestre
- [ ] Mínimo 2 exemplos aprovados em `examples/` (quando aplicável)
- [ ] Rubrica de avaliação presente no arquivo
- [ ] Score médio >= 8.0/10 na rubrica geral (`evals/rubrica-geral.md`)
- [ ] Nenhum critério crítico abaixo de 7.0/10
- [ ] Revisão comercial feita (Rayanne Gama Imóveis)
- [ ] Revisão técnica feita (Automab.dev)
- [ ] ADR registrado se a skill representar decisão arquitetural


## Contexto (context/)

Para um documento de contexto ser considerado pronto:

- [ ] Todas as seções obrigatórias preenchidas
- [ ] Aprovado pela Rayanne Gama Imóveis
- [ ] Exemplos de tom de voz: bom × ruim presentes
- [ ] Pelo menos 2 personas completas
- [ ] Funil mapeado com eventos de conversão
- [ ] Glossário PT-BR imobiliário revisado

## ADR (adr/)

Para um ADR ser considerado pronto:

- [ ] Status: `accepted`
- [ ] Contexto, decisão e consequências documentados
- [ ] Alternativas consideradas listadas
- [ ] Data e responsável registrados

## Exemplo (examples/)

Para um exemplo ser considerado aprovado:

- [ ] Baseado em caso real ou realista de uso
- [ ] Revisado por pelo menos um dos responsáveis
- [ ] Classificado por: skill, persona, canal, tipo de imóvel
- [ ] Score >= 8.0 na rubrica geral

## Eval (evals/)

Para um caso de eval ser considerado pronto:

- [ ] Input completo e realista
- [ ] Output esperado descrito
- [ ] Critérios de reprovação automática listados
- [ ] Avaliador designado (técnico, comercial ou ambos)

## Integração (integrations/)

Para uma integração ser considerada pronta:

- [ ] Schema ou contrato de dados documentado
- [ ] Evento ou campo testado em ambiente real
- [ ] Responsável por manutenção definido
