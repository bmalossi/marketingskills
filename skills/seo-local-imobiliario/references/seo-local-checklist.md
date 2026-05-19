# SEO Local — Estrutura de Busca e Checklist

Referência operacional para otimização de buscas locais baseada em parâmetros dinâmicos.

---

## Estrutura de URLs de Busca

O site utiliza um sistema único de busca dinâmica. Não existem páginas estáticas separadas para cada cidade ou bairro; tudo é filtrado via parâmetros na URL `/imoveis`.

### Parâmetros Principais

| Parâmetro | Descrição | Exemplo |
|-----------|-----------|---------|
| `cidade` | Filtro por município | `?cidade=praia+grande` |
| `busca` | Filtro por bairro ou termo | `&busca=guilhermina` |
| `dormitorios` | Filtro por nº de quartos | `&dormitorios=2` |
| `tipo` | Tipo de imóvel | `&tipo=Apartamento` |
| `transacao` | Venda ou Aluguel | `&transacao=venda` |

### Exemplos de URLs Canônicas para SEO e Ads

| Objetivo | URL Estruturada |
|----------|-----------------|
| Imóveis em Praia Grande | `/imoveis?cidade=praia+grande` |
| Imóveis em São Vicente | `/imoveis?cidade=são+vicente` |
| Imóveis no Boqueirão (PG) | `/imoveis?cidade=praia+grande&busca=boqueirão` |
| Imóveis no Canto do Forte | `/imoveis?cidade=praia+grande&busca=canto+do+forte` |
| Aptos 1 dorm no Boqueirão | `/imoveis?cidade=praia+grande&dormitorios=1&tipo=Apartamento&busca=boqueirão` |

> [!IMPORTANT]
> Como o site não possui páginas estáticas para cada filtro, o SEO local deve focar na indexação da página de busca com parâmetros ou no uso dessas URLs em campanhas de tráfego pago e redes sociais.

---

## Checklist de Qualidade SEO (Página de Busca)

### On-Page Essentials (Filtros Dinâmicos)
- [ ] Os parâmetros de URL são limpos e legíveis
- [ ] O título da página reflete o filtro aplicado (ex: "Imóveis à venda em Praia Grande - Boqueirão")
- [ ] Meta description dinâmica baseada nos filtros
- [ ] Schema markup `ItemList` para resultados de busca
- [ ] Link canônico apontando para a URL de busca principal
- [ ] Botão WhatsApp visível e funcional em todas as telas de resultado

### Sinais de Qualidade e Conteúdo
- [ ] A listagem de imóveis é relevante para o termo de busca/parâmetro
- [ ] O usuário consegue identificar rapidamente o diferencial da Rayanne Gama (Atendimento Humano)
- [ ] Filtros laterais ou superiores fáceis de usar em mobile

---

## Google Business Profile — Rotina Mensal

| Ação | Frequência |
|------|-----------|
| Publicar post no GBP (imóvel ou dica) | Semanal |
| Responder todas as avaliações (positivas e negativas) | Em até 48h |
| Atualizar fotos do perfil e serviços | Mensal |
| Verificar consistência NAP (Nome, Endereço, Telefone) | Mensal |
| Monitorar insights (buscas, visualizações, cliques) | Mensal |

---

## NAP Padrão — Rayanne Gama Imóveis

> Usar exatamente este formato em todos os diretórios e o site:

```
Nome: Rayanne Gama Imóveis
Endereço: Rua Dr José Carlos de Oliveira, 274 - Boqueirão, Praia Grande/SP
Telefone: (13) 99768-5529
Site: https://rayannegamaimoveis.com.br
```

> [!CAUTION]
> Inconsistência no NAP entre o site e diretórios externos prejudica o ranqueamento local. Verificar sempre antes de cadastrar em novo diretório.
