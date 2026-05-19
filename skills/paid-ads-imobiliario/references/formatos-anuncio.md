# Formatos de Anúncio — Paid Ads Imobiliário

Referência de formatos, specs e melhores práticas para Meta Ads e Google Ads da Rayanne Gama Imóveis.

---

## Meta Ads (Facebook + Instagram)

### Formatos Recomendados por Objetivo

| Objetivo | Formato Recomendado | Por quê |
|----------|--------------------|---------| 
| Gerar leads de primeiro imóvel | Vídeo curto (15–30s) + CTA WhatsApp | Maior alcance, perfil emocional |
| Apresentar imóvel específico | Carrossel com fotos reais (3–7 fotos) | Mostra múltiplos ambientes |
| Remarketing (quem visitou o site) | Post único com copy de reconexão | Simples e direto |
| Lançamento de empreendimento | Vídeo de 45–60s + lead form | Gera expectativa, captura dados |
| Conteúdo educativo (FGTS, MCMV) | Reels 15–30s ou carrossel | Alto compartilhamento |

---

### Especificações Técnicas

#### Vídeo (Feed + Reels)
- Formato: Vertical (9:16) ou Quadrado (1:1) para feed
- Duração: 15–30s para topo de funil; até 60s para lançamentos
- Legenda: obrigatória (50%+ assiste sem som)
- Gancho: primeiros 3 segundos determinam se o usuário continua
- Arquivo: MP4, mínimo 720p

#### Carrossel
- Número de cards: 3 a 7
- Proporção: 1:1 (quadrado) ou 4:5
- Resolução: mínimo 1080x1080px
- Texto na imagem: < 20% da área (regra Meta)
- Ordem sugerida: exterior → sala → quartos → cozinha → varanda → CTA

#### Post Único (Imagem)
- Proporção: 4:5 (portrait) para feed Instagram
- Resolução: 1080x1350px
- Texto na imagem: mínimo possível; headline pode aparecer, mas evitar blocos de texto

---

### Estrutura do Copy de Anúncio

```
[GANCHO — 1 frase, máximo 15 palavras]
[BENEFÍCIO PRINCIPAL — 1 ou 2 frases]
[PROVA / CONTEXTO LOCAL]
[CTA]
```

**Exemplo aprovado:**
> Apartamento de 2 dormitórios a 3 quadras do mar em Guilhermina, Praia Grande.
> Financiamento facilitado — a gente te ajuda com Caixa, FGTS e MCMV.
> 👇 Chama no WhatsApp e recebe as fotos hoje.

**Exemplo que NÃO deve ser usado:**
> ❌ "OPORTUNIDADE ÚNICA!! Incrível apto em PG!! Não perca!! Chama AGORA!!"

---

### Segmentação Base por Persona

| Persona | Faixa etária | Interesses | Localização |
|---------|-------------|------------|-------------|
| Primeiro imóvel | 22–35 | "Imóveis", "Caixa Econômica", "Casa própria" | Praia Grande + 20km |
| Família upgrade | 30–50 | "Imóveis", "Família", "Decoração" | Praia Grande + cidades vizinhas |
| Investidor | 35–60 | "Investimento imobiliário", "Renda passiva" | SP capital + Baixada Santista |
| Remarketing | — | Visitantes do site (Custom Audience) | Qualquer lugar |

---

## Google Ads (Search)

### Estrutura de Campanha Recomendada

```
Campanha: [Objectivo] — [Cidade]
  Grupo 1: Compra — Apartamento Praia Grande
    KW: "apartamento à venda praia grande" [exata]
    KW: "comprar apartamento praia grande sp" [frase]
    KW: "apt 2 dormitorios praia grande" [frase]
  Grupo 2: Financiamento — Praia Grande
    KW: "financiamento imobiliario praia grande" [exata]
    KW: "mcmv praia grande" [frase]
    KW: "caixa economica apartamento praia grande" [frase]
  Grupo 3: Imóvel Específico
    KW: [bairro + tipologia] — criado por lançamento
```

### Especificações do Anúncio Responsivo (RSA)

| Campo | Limite | Recomendação |
|-------|--------|-------------|
| Headlines | 30 caracteres (até 15) | Usar ao menos 3 com palavra-chave |
| Descrições | 90 caracteres (até 4) | Mencionar financiamento e WhatsApp |

**Headlines aprovadas:**
```
Apartamento em Praia Grande
2 Dorm. a partir de R$ 250mil
Financiamento Caixa e MCMV
Fale com Correspondente Direto
Imóveis na Baixada Santista
```

**Descrições aprovadas:**
```
Atendimento humano do começo ao fim. Correspondente bancário direto. Fale no WhatsApp.
Imóveis em Praia Grande, São Vicente, Santos e Mongaguá. Simule sem compromisso.
```

### Extensões Obrigatórias

- **Extensão de local:** endereço físico da imobiliária
- **Extensão de chamada:** número de WhatsApp
- **Extensão de sitelink:** Imóveis, Financiamento, Contato, MCMV
- **Extensão de snippets estruturados:** Praia Grande, São Vicente, Santos, Mongaguá

---

## Checklist de Qualidade — Antes de Publicar

### Meta Ads
- [ ] Pixel Meta instalado e disparando `click_whatsapp` e `form_submit`
- [ ] Copy sem clichês proibidos (oportunidade única, não perca, etc.)
- [ ] Texto na imagem < 20%
- [ ] CTA claro e testado
- [ ] Público segmentado por persona (não "todos over 18")
- [ ] Campanha com 1 objetivo único
- [ ] UTMs configurados no link de destino

### Google Ads
- [ ] Extensões de local e chamada configuradas
- [ ] Página de destino específica (não a home)
- [ ] Conversion tracking ativo (GA4 + Google Tag)
- [ ] Palavras-chave negativas configuradas (ex: "aluguel", "grátis")
- [ ] Headlines com palavra-chave da busca
