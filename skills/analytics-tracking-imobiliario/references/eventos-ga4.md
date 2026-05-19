# Eventos GA4 e Meta Pixel — Rayanne Gama Imóveis

Referência de implementação de rastreamento para o site rayannegamaimoveis.com.br.

---

## Eventos Obrigatórios (GA4 + Meta Pixel)

Esta é a lista canônica de eventos definida no contexto mestre. Todos os eventos devem estar configurados antes de rodar qualquer campanha paga.

| Evento | Trigger | Valor Estimado da Conversão |
|--------|---------|----------------------------|
| `view_listing` | Carregar página de imóvel | Baixo |
| `click_whatsapp` | Clique em qualquer botão WhatsApp do site | **Alto** |
| `form_submit` | Envio de qualquer formulário de contato | **Alto** |
| `schedule_visit` | Agendamento de visita confirmado | **Muito alto** |
| `request_simulation` | Solicitação de simulação de financiamento | **Muito alto** |
| `proposal_sent` | Proposta enviada (evento manual/CRM) | Muito alto |
| `sale_closed` | Venda fechada (evento manual/CRM) | Máximo |

> **Eventos principais de conversão para otimização de anúncio:** `click_whatsapp` + `form_submit`

---

## Configuração via Google Tag Manager (GTM)

### 1. `click_whatsapp`

**Trigger:** Clique em link contendo `wa.me` ou `api.whatsapp`

```javascript
// No GTM: Tag de Evento GA4
Event Name: click_whatsapp
Parameters:
  - source: {{Page URL}}
  - button_location: {{Click Text}} ou {{Click ID}}
```

**Meta Pixel:** `fbq('track', 'Contact')` no mesmo trigger.

---

### 2. `form_submit`

**Trigger:** Submissão de formulário (evento de formulário do GTM ou URL de obrigado)

```javascript
// GA4 Event
Event Name: form_submit
Parameters:
  - form_id: {{Form ID}}
  - page_location: {{Page URL}}

// Meta Pixel
fbq('track', 'Lead')
```

---

### 3. `view_listing`

**Trigger:** Page View nas URLs que contêm `/imoveis/` ou `/imoveis/[slug]/`

```javascript
Event Name: view_listing
Parameters:
  - listing_id: {{URL}} // extrair do path
  - listing_city: Praia Grande // preencher via variável de dataLayer
```

---

### 4. `schedule_visit`

**Trigger:** Clique no botão "Agendar visita" ou URL de confirmação de agendamento

```javascript
Event Name: schedule_visit
// Meta Pixel
fbq('track', 'Schedule')
```

---

## UTM Parameters — Padrão para Campanhas

Usar sempre UTM em links de campanhas para atribuição correta no GA4.

| Campo | Padrão para Meta Ads | Padrão para Google Ads |
|-------|---------------------|----------------------|
| `utm_source` | `facebook` ou `instagram` | `google` |
| `utm_medium` | `paid_social` | `cpc` |
| `utm_campaign` | `[nome-da-campanha]` | `[nome-da-campanha]` |
| `utm_content` | `[criativo-ou-adset]` | `[grupo-de-anuncio]` |
| `utm_term` | — | `[palavra-chave]` |

**Exemplo:**
```
https://rayannegamaimoveis.com.br/imoveis?cidade=praia+grande
&utm_source=facebook
&utm_medium=paid_social
&utm_campaign=lancamento-guilhermina-jun26
&utm_content=video-casal-jovem
```

---

## Dashboard Semanal — Métricas Prioritárias

| Métrica | Fonte | Meta |
|---------|-------|------|
| Sessões totais | GA4 | — |
| Taxa de clique no WhatsApp | GA4 (`click_whatsapp` / sessões) | **> 4%** |
| Taxa de envio de formulário | GA4 (`form_submit` / sessões) | **> 2%** |
| Leads por canal (Meta, Google, Orgânico) | GA4 + Planilha | — |
| Custo por lead (CPL) | Meta Ads Manager / Google Ads | Definir após piloto |
| Taxa de agendamento por lead | Planilha CRM | **> 15%** |

> Fonte das metas: `context/product-marketing-context-rayanne-ptbr.md`

---

## Integração WhatsApp → GA4

O WhatsApp não retorna dados de conversão automaticamente ao GA4. Para rastrear leads originados de cliques no WhatsApp:

1. **Configurar evento `click_whatsapp`** no GTM (já descrito acima)
2. **Registrar leads no CRM** com canal de origem (preenchido pelo corretor)
3. **Usar Conversions API (CAPI) do Meta** para enviar eventos de backend (após a visita ou proposta) — integração avançada, recomendada quando volume justificar

---

## Ferramentas e Acessos

| Ferramenta | Uso | Status |
|------------|-----|--------|
| Google Tag Manager | Implementação de eventos | [TODO — verificar acesso] |
| GA4 Property | Analytics | [TODO — verificar ID da propriedade] |
| Meta Pixel | Remarketing e otimização de anúncios | [TODO — verificar ID do pixel] |
| Google Search Console | SEO e indexação | [TODO — verificar acesso] |
| Looker Studio | Dashboard | [TODO — criar ou conectar] |
