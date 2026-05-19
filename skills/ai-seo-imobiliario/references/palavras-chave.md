# Palavras-Chave SEO Local — Rayanne Gama Imóveis

Referência de termos por cidade, tipo e intenção para otimização de conteúdo e anúncios.

---

## Clusters de Busca por Cidade

### Praia Grande/SP (Prioridade 1)
```
apartamento à venda Praia Grande
casa à venda Praia Grande SP
imóveis Praia Grande SP
comprar apartamento Praia Grande
imobiliária Praia Grande SP
apartamento 2 dormitórios Praia Grande
apartamento financiamento Praia Grande
MCMV Praia Grande
apartamento Guilhermina Praia Grande
apartamento Caiçara Praia Grande
apartamento Aviação Praia Grande
apartamento Boqueirão Praia Grande
```

### São Vicente/SP (Prioridade 2)
```
apartamento à venda São Vicente SP
imóveis São Vicente SP
casa à venda São Vicente
imobiliária São Vicente SP
```

### Santos/SP (Prioridade 3)
```
imóveis Santos SP
apartamento Santos à venda
imobiliária Santos SP
apartamento alto padrão Santos
```

### Mongaguá/SP (Prioridade 4)
```
apartamento à venda Mongaguá
casa Mongaguá SP
MCMV Mongaguá
imóveis Mongaguá
```

---

## Clusters de Busca por Situação

### Financiamento e Crédito
```
financiamento imobiliário Praia Grande
Caixa Econômica Federal imóvel Praia Grande
MCMV Praia Grande apartamento
Minha Casa Minha Vida Praia Grande
usar FGTS para comprar imóvel
como financiar apartamento Praia Grande
simulação financiamento imobiliário
aprovação crédito imobiliário
```

### Primeiro Imóvel
```
como comprar primeiro imóvel
primeiro imóvel financiamento
imóvel para quem não tem entrada
apartamento acessível Praia Grande
como usar FGTS para comprar apartamento
```

### Investimento
```
apartamento para investir Praia Grande
imóvel para alugar Praia Grande
rendimento aluguel praia grande
investimento imobiliário Baixada Santista
imóvel segunda residência Praia Grande
```

---

## Schema Markup Obrigatório

| Página | Schema |
|--------|--------|
| Cada imóvel | `RealEstateListing` |
| Página institucional/equipe | `RealEstateAgent` |
| Home + Rodapé | `LocalBusiness` |
| Blog/artigos | `Article` |

### Dados mínimos do `RealEstateListing`
```json
{
  "@type": "RealEstateListing",
  "name": "[Título do imóvel]",
  "description": "[Descrição]",
  "url": "[URL da página]",
  "price": "[Valor]",
  "priceCurrency": "BRL",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Endereço]",
    "addressLocality": "Praia Grande",
    "addressRegion": "SP",
    "postalCode": "[CEP]",
    "addressCountry": "BR"
  }
}
```

---

## Intenções de Busca Prioritárias

| Intenção | Exemplo de Busca | Tipo de Página |
|----------|-----------------|----------------|
| Comprar | "apartamento à venda Praia Grande" | Listagem/Landing |
| Financiar | "como financiar imóvel em Praia Grande" | Artigo/FAQ |
| Saber valor | "apartamento 2 dormitórios preço Praia Grande" | Listagem |
| Contatar | "imobiliária Praia Grande telefone" | Google Business |
| Aprender | "como usar FGTS para comprar imóvel" | Blog |
