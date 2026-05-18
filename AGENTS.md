# AGENTS.md — Rayanne Gama Imóveis

> Este arquivo orienta agentes de IA sobre como operar neste repositório.
> Leia este arquivo antes de qualquer tarefa de marketing.

## Identidade do Projeto

Este repositório contém skills de marketing especializadas para a **Rayanne Gama Imóveis**, uma imobiliária localizada na região de Campinas/SP, Brasil. Todo conteúdo gerado deve refletir o posicionamento, o tom de voz e os objetivos comerciais desta imobiliária.

## Regras Gerais

1. **Sempre leia o contexto mestre primeiro:** `context/product-marketing-context-rayanne-ptbr.md`
2. **Nunca invente dados:** Se não houver informação suficiente nos inputs, pergunte antes de gerar.
3. **Idioma:** Todo output de marketing deve ser em **PT-BR**, com vocabulário imobiliário brasileiro.
4. **Tom:** Profissional, acolhedor, direto. Sem exageros, superlativos vazios ou clichês de anúncio.
5. **CTA obrigatório:** Todo ativo de marketing (copy, post, anúncio, landing) deve ter um CTA claro — WhatsApp, formulário ou agendamento.
6. **Persona:** Sempre identifique a persona-alvo antes de gerar qualquer conteúdo.
7. **Canal:** Adapte linguagem, tamanho e formato ao canal especificado no input.

## Palavras e Expressões a Evitar

- "Realize o sonho da casa própria" — clichê
- "Oportunidade única" — sem evidência
- "Não perca!" — sensacionalismo
- "O melhor da região" — sem prova
- Termos em inglês no copy final (ex: "lifestyle", "home office" — use versão PT-BR quando possível)

## Funil de Conversão

O funil da Rayanne Gama Imóveis tem as seguintes etapas e eventos:

```
Descoberta → Consideração → Intenção → Proposta → Venda
    ↓              ↓            ↓          ↓         ↓
view_listing  click_whatsapp  schedule  proposal   sale
              form_submit     visit     _sent      _closed
                              request
                              _simulation
```

Todo conteúdo deve ser orientado a mover o lead para a próxima etapa do funil.

## Uso das Skills

- Antes de usar uma skill, verifique se o status é `approved` no frontmatter do SKILL.md
- Skills com status `draft` ou `review` não devem ser usadas em produção
- Se a skill mais adequada ainda não existe ou está em draft, sinalize e use o melhor julgamento baseado no contexto mestre

## Avaliação de Output

Todo output gerado deve ser auto-avaliado antes de ser entregue, usando a rubrica em `evals/rubrica-geral.md`. Se o score estimado for abaixo de 7.0 em qualquer critério crítico, refaça antes de entregar.

## Quando Pedir Ajuda

Peça input humano quando:
- O contexto mestre não tiver informação suficiente para a tarefa
- A persona alvo não estiver clara
- O canal ou objetivo não estiver especificado
- O output envolver dados reais de preço, localização ou características do imóvel

## Contato dos Responsáveis

| Papel | Responsável |
|-------|------------|
| Arquitetura e IA | Automab.dev |
| Validação comercial | Rayanne Gama Imóveis |
