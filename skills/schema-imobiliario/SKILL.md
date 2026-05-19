---
name: schema-imobiliario
description: Define marcação de dados estruturados para o site da Rayanne Gama Imóveis em PT-BR, com foco em imóveis, negócios locais e páginas de conteúdo.
status: approved
last_updated: 2026-05-19
---

# Schema Imobiliário PT-BR

Use esta skill quando o pedido envolver dados estruturados, rich results ou organização semântica do site da Rayanne Gama Imóveis.

## Objetivo
Ajudar buscadores a entender melhor o conteúdo do site e aumentar a chance de destaque em resultados relevantes.

## Quando usar
- Marcações para páginas do site.
- Dados estruturados para imóveis.
- Organização semântica de conteúdo.
- Otimização de páginas locais.
- Páginas de blog e FAQ.

## Inputs mínimos
- Tipo de página.
- Conteúdo principal.
- Cidade ou bairro.
- Tipo de imóvel.
- Objetivo da página.

## Contexto da marca
- Nome: Rayanne Gama Imóveis.
- Site: rayannegamaimoveis.com.br.
- Atuação prioritária: Praia Grande/SP.
- Outras regiões: São Vicente, Santos, Mongaguá e Interior de SP.
- Tipos de imóvel: apartamentos, casas, terrenos, comerciais e lançamentos.

## Processo
1. Identifique o tipo de página.
2. Escolha o schema mais apropriado.
3. Preencha os campos essenciais.
4. Garanta consistência entre schema e conteúdo visível.
5. Sugira validação técnica antes de publicar.

## Tipos de schema úteis
- RealEstateListing.
- Product, quando fizer sentido para anúncio de imóvel.
- LocalBusiness.
- Organization.
- FAQPage.
- BreadcrumbList.
- Article.
- WebPage.

## Regras de implementação
- O schema deve refletir o conteúdo real da página.
- Não invente dados estruturados.
- Evite marcação excessiva ou inconsistente.
- Combine schema com SEO local e arquitetura do site.
- Use apenas campos que possam ser mantidos atualizados.

## Checklist de qualidade
- O schema corresponde ao conteúdo visível.
- Os campos essenciais estão preenchidos.
- A marcação ajuda a entender a página.
- O uso do schema é compatível com o tipo de página.
- Existe consistência entre SEO e dados estruturados.

## Formato de saída
Entregar sempre em um destes formatos:
- lista de schemas recomendados.
- mapa de campos.
- exemplo de JSON-LD.
- checklist de validação.

## Limites
Se faltar informação essencial, peça:
- tipo de página.
- conteúdo visível.
- cidade ou bairro.
- tipo de imóvel.