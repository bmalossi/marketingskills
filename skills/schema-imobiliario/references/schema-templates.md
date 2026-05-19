# Schema Markup — Templates JSON-LD

Templates prontos para implementação nas principais páginas do site da Rayanne Gama Imóveis.
Copiar, preencher os campos marcados com `[PREENCHER]` e adicionar via `<script>` no `<head>`.

---

## Template 1 — RealEstateListing (Página de Imóvel)

Usar em cada página individual de imóvel.

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "RealEstateListing",
  "name": "[PREENCHER — ex: Apartamento 2 Dormitórios em Guilhermina]",
  "description": "[PREENCHER — descrição de 100-150 palavras do imóvel]",
  "url": "[PREENCHER — URL completa da página do imóvel]",
  "datePosted": "[PREENCHER — YYYY-MM-DD]",
  "price": "[PREENCHER — valor em número, sem R$ ou pontos]",
  "priceCurrency": "BRL",
  "floorSize": {
    "@type": "QuantitativeValue",
    "value": "[PREENCHER — ex: 65]",
    "unitCode": "MTK"
  },
  "numberOfRooms": "[PREENCHER — número de dormitórios]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[PREENCHER — ex: Avenida Presidente Kennedy]",
    "addressLocality": "[PREENCHER — ex: Praia Grande]",
    "addressRegion": "SP",
    "postalCode": "[PREENCHER — CEP]",
    "addressCountry": "BR"
  },
  "offers": {
    "@type": "Offer",
    "price": "[PREENCHER — valor]",
    "priceCurrency": "BRL",
    "availability": "https://schema.org/InStock"
  },
  "offeredBy": {
    "@type": "RealEstateAgent",
    "name": "Rayanne Gama Imóveis",
    "url": "https://rayannegamaimoveis.com.br",
    "telephone": "[PREENCHER]"
  }
}
</script>
```

---

## Template 2 — RealEstateAgent (Página Institucional / Sobre)

Usar na página "Sobre a Rayanne Gama" ou página inicial.

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "RealEstateAgent",
  "name": "Rayanne Gama Imóveis",
  "url": "https://rayannegamaimoveis.com.br",
  "logo": "https://rayannegamaimoveis.com.br/logo.png",
  "image": "https://rayannegamaimoveis.com.br/foto-equipe.jpg",
  "description": "Imobiliária especializada em Praia Grande e Baixada Santista, com 5 anos de mercado. Correspondente bancário direto — auxiliamos em financiamento Caixa, MCMV e FGTS.",
  "telephone": "[PREENCHER]",
  "email": "[PREENCHER]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[PREENCHER]",
    "addressLocality": "Praia Grande",
    "addressRegion": "SP",
    "postalCode": "[PREENCHER]",
    "addressCountry": "BR"
  },
  "openingHours": "Mo-Fr 09:00-18:00, Sa 09:00-13:00",
  "areaServed": [
    "Praia Grande",
    "São Vicente",
    "Santos",
    "Mongaguá",
    "Bertioga"
  ],
  "sameAs": [
    "[PREENCHER — URL do Instagram]",
    "[PREENCHER — URL do Facebook]",
    "[PREENCHER — URL do Google Business]"
  ]
}
</script>
```

---

## Template 3 — LocalBusiness (Home / Rodapé)

Complementar ao RealEstateAgent. Adicionar na home.

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Rayanne Gama Imóveis",
  "url": "https://rayannegamaimoveis.com.br",
  "telephone": "[PREENCHER]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[PREENCHER]",
    "addressLocality": "Praia Grande",
    "addressRegion": "SP",
    "postalCode": "[PREENCHER]",
    "addressCountry": "BR"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "-24.0059",
    "longitude": "-46.4027"
  },
  "openingHours": "Mo-Fr 09:00-18:00 Sa 09:00-13:00",
  "priceRange": "R$ 100.000 a R$ 2.000.000"
}
</script>
```

> **Coordenadas geo:** Latitude `-24.0059`, Longitude `-46.4027` são as coordenadas do centro de Praia Grande. Ajustar para o endereço exato da imobiliária.

---

## Template 4 — Article (Artigos do Blog)

Usar em cada post do blog.

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "[PREENCHER — título do artigo]",
  "description": "[PREENCHER — resumo de 150 caracteres]",
  "datePublished": "[PREENCHER — YYYY-MM-DD]",
  "dateModified": "[PREENCHER — YYYY-MM-DD]",
  "url": "[PREENCHER — URL do artigo]",
  "author": {
    "@type": "Organization",
    "name": "Rayanne Gama Imóveis"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Rayanne Gama Imóveis",
    "logo": {
      "@type": "ImageObject",
      "url": "https://rayannegamaimoveis.com.br/logo.png"
    }
  },
  "image": "[PREENCHER — URL da imagem principal do artigo]"
}
</script>
```

---

## Validação

Testar todos os schemas em: **https://search.google.com/test/rich-results**

| Tipo de Página | Schema | Testado? |
|----------------|--------|----------|
| Home | LocalBusiness + RealEstateAgent | [TODO] |
| Sobre | RealEstateAgent | [TODO] |
| Imóvel individual | RealEstateListing | [TODO] |
| Blog / Artigo | Article | [TODO] |

> [!CAUTION]
> Use o Google Rich Results Test para validar antes de publicar. Schemas com erros podem ser ignorados pelo Google.
