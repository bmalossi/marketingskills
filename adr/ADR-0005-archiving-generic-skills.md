# ADR-0005 — Arquivamento das Skills Genéricas do Fork Original

- **Status:** Accepted
- **Data:** 2026-05-19
- **Decisor:** Automab.dev + Rayanne Gama Imóveis

## Contexto

Este repositório é um fork de `coreyhaines31/marketingskills`. O fork original continha 40 skills de marketing genéricas desenvolvidas para produtos SaaS e B2B em inglês. Ao adaptar o repositório para a Rayanne Gama Imóveis (imobiliária PT-BR), essas skills genéricas tornaram-se irrelevantes para o fluxo operacional e potencialmente causadoras de confusão para agentes de IA.

## Decisão

Mover todas as 40 skills genéricas para `skills/archive/`, mantendo-as no repositório por motivos históricos, mas removendo-as do fluxo ativo de uso.

## Alternativas consideradas

| Alternativa | Motivo de descarte |
|-------------|-------------------|
| Deletar as skills | Perda do histórico e referência útil para futuras adaptações |
| Manter junto com skills imobiliárias | Confunde agentes de IA; polui a navegação |
| Marcar apenas como deprecated no SKILL.md | Insuficiente — ainda apareceriam ao listar skills/ |

## Consequências

**Positivas:**
- `skills/` contém apenas skills imobiliárias ativas
- Agentes de IA não confundem contexto SaaS com imobiliário
- Navegação limpa e consistente com o propósito do fork

**Negativas:**
- Skills genéricas não são mais acessíveis diretamente no fluxo de skills
- Qualquer reutilização futura exige mover a pasta de volta ou criar versão imobiliária

## Regra de manutenção

Para criar uma nova skill a partir de uma genérica arquivada:
1. Copiar a pasta de `skills/archive/<skill>/` para `skills/<skill>-imobiliario/`
2. Adaptar o SKILL.md ao contexto da Rayanne Gama Imóveis
3. Criar evals/ e references/ imobiliários
4. Registrar a decisão de reativação neste ADR ou em um novo ADR
