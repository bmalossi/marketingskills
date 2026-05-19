# Métricas e Funil de Vendas — Rayanne Gama Imóveis

Referência operacional para RevOps: funil, SLAs, eventos de GA4 e rotina de acompanhamento.

---

## Funil de Vendas

```
Descoberta → Consideração → Intenção → Proposta → Venda
     ↓              ↓            ↓          ↓         ↓
view_listing  click_whatsapp  schedule  proposal   sale
              form_submit     _visit    _sent      _closed
                              request
                              _simulation
```

### Etapas e Critérios de Qualificação

| Etapa | Definição | Critério de Avanço |
|-------|-----------|-------------------|
| Lead Novo | Primeiro contato realizado | Respondeu e foi qualificado |
| Lead Qualificado | Tem objetivo, prazo e budget | Agendou visita ou pediu simulação |
| Visita Agendada | Confirmou data e horário | Compareceu à visita |
| Proposta Enviada | Recebeu proposta formal | Resposta à proposta |
| Em Negociação | Está negociando termos | — |
| Venda Fechada | Contrato assinado | — |
| Perdido | Desistiu, sem crédito, comprou outro | Registrar motivo |

---

## SLAs de Atendimento

| Canal | SLA de Primeira Resposta |
|-------|-------------------------|
| WhatsApp | ≤ 5 minutos (horário comercial) |
| Instagram DM | ≤ 10 minutos |
| Facebook Messenger | ≤ 15 minutos |
| Formulário do site | ≤ 30 minutos |
| OLX / ZAP / VivaReal | ≤ 20 minutos |

> **Regra:** Lead sem resposta em 30 minutos durante horário comercial tem 40% menos chance de conversão.

---

## Critérios de SQL (Lead Qualificado)

Um lead é SQL quando:
- [ ] Tem objetivo claro (comprar, locar ou investir)
- [ ] Tem prazo definido (imediatamente a 12 meses)
- [ ] Faixa de valor compatível com portfólio (R$ 100k a R$ 2M)
- [ ] Situação de crédito não é bloqueante (ou pode ser trabalhada com correspondente)
- [ ] Demonstrou intenção real (quer visita, simulação ou mais informação específica)

---

## Eventos de Conversão (GA4 + Meta Pixel)

| Evento | Descrição | Valor estimado |
|--------|-----------|---------------|
| `view_listing` | Visualizou página de imóvel | Baixo |
| `click_whatsapp` | Clicou no botão WhatsApp | Médio |
| `form_submit` | Enviou formulário de contato | Médio-alto |
| `schedule_visit` | Agendou visita | Alto |
| `request_simulation` | Pediu simulação de financiamento | Alto |
| `proposal_sent` | Proposta enviada | Muito alto |
| `sale_closed` | Venda fechada | Evento principal |

---

## Rotina Operacional Semanal

| Quando | O que fazer |
|--------|-------------|
| Segunda (manhã) | Revisar todos os leads abertos, definir próximas ações |
| Durante semana | Atualizar CRM a cada atendimento |
| Sexta (fim do dia) | Revisar funil: quantos avançaram, quantos perdemos |
| Mensal | Calcular taxas de conversão por etapa e canal |

---

## KPIs de Canal (Metas Iniciais)

| KPI | Meta |
|-----|------|
| CTR anúncio Meta Ads | > 2% |
| CTR anúncio Google Ads | > 5% |
| Taxa de clique no WhatsApp (site) | > 4% das sessões |
| Taxa de envio de formulário | > 2% das sessões |
| Taxa de agendamento por lead | > 15% |
| Taxa de SQL (lead qualificado) | > 40% dos leads |

> Fonte: `context/product-marketing-context-rayanne-ptbr.md`

---

## Motivos de Perda (Registrar Sempre)

- Crédito não aprovado
- Não tem entrada suficiente
- Comprou com outro corretor
- Não encontrou imóvel adequado no portfólio
- Mudou de ideia (alugar em vez de comprar)
- Sem resposta após múltiplas tentativas
- Prazo muito longo (mais de 12 meses)
