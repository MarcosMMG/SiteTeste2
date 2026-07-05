# Plano — Site JEMAC (v2 — storytelling + conversão + SEO)

> Referência visual: https://storytelling.noomoagency.com/
> Status: **v1 construída** em `site/` (Hero, Dor, Serviços, Como Funciona, CTA, Footer).
> Este plano cobre o que falta pra virar máquina de captação.
> Atualizado em 2026-07-04 (pesquisa de melhores práticas de conversão incluída).

---

## 1. Objetivo único

Uma página, uma ação: visitante clicar **"Peça seu orçamento"** → WhatsApp
(21) 96515-6359. Tudo no site serve a esse clique.

- Vende: criação de site, Google Meu Negócio, Google Ads, Google Local (SEO)
- Público: dono de pequena empresa em **todo o Brasil** (atendimento remoto), leigo em tecnologia. Base física: RJ — usar como sinal de confiança, não como limite
- Preço: nunca aparece — sempre "peça um orçamento"

## 2. Conceito / narrativa

Metáfora: **beija-flor origami subindo ao topo** = cliente saindo da
invisibilidade pro 1º lugar do Google. Scroll conta a história em 3 atos:

1. **Dor** — "Sua empresa existe, mas ninguém te acha."
2. **Jornada** — o que a JEMAC faz; pássaro ganha altura.
3. **Topo** — "Do invisível ao topo do Google." CTA.

Tom: confiança e segurança (ver `preferencias.md`). Sem promessa de guru,
sem jargão.

---

## 3. Regras de copy (validadas por pesquisa de conversão)

- Headline com menos de 10 palavras, benefício claro
  (atual: "Sua empresa existe. Só falta o Google saber disso." — manter)
- **1 CTA único repetido** — sem menu de navegação (páginas sem menu
  convertem até 2x mais)
- CTA sempre visível acima da dobra
- Depoimento com **número real** vale mais que elogio genérico
  ("dobrou os pedidos" > "ótimo serviço")
- Formulário: quanto mais curto melhor — WhatsApp direto é o ideal
- Zero jargão técnico, zero "alavancar/explodir vendas"

---

## 4. Estrutura da página (ordem do scroll)

| # | Seção | Conteúdo | Status |
|---|-------|----------|--------|
| 1 | Hero | Headline + pássaro + CTA + micro-sinais de confiança | ✅ feita |
| 2 | A dor | "Você tá invisível no Google" | ✅ feita |
| 3 | Serviços | 4 cards (site, GMB, Ads, Google Local) | ✅ feita |
| 4 | Como funciona | 3 passos: diagnóstico → site+SEO → topo | ✅ feita |
| 5 | Portfólio | Case real: Um Lugar Encantado (card com link ao vivo) | ✅ feita (trocar preview CSS por screenshot real depois) |
| 6 | Por que a JEMAC | 3 pilares de confiança (sem depoimento fake) | ✅ feita (trocar por depoimentos reais no 1º cliente) |
| 7 | FAQ | 6 perguntas em accordion + schema FAQPage | ✅ feita |
| 8 | CTA final | "Do invisível ao topo do Google" + WhatsApp | ✅ feita |
| 9 | Footer | Contato, base RJ + Brasil, logo-branco | ✅ feita |

---

## 5. Confiança — prioridade máxima

Trust signals acima da dobra elevam conversão 20-40%. Escada:

1. **Agora (sem clientes):** micro-sinais no hero —
   "Atendimento direto com quem faz", "Atendimento em todo o Brasil",
   "Ajustes até você aprovar" (garantia simples).
2. **Primeiro cliente:** depoimento com número + print de avaliação
   Google. Substitui placeholder do portfólio por case real.
3. **GMB da própria JEMAC** com avaliações — vitrine do serviço que
   vende. Prioridade fora do site também.

---

## 6. Camada SEO

### 6.1 Técnico
- HTML semântico (1 H1, hierarquia H2/H3) — ✅ já ok na v1
- sitemap.xml + robots.txt — ❌ falta
- lang="pt-BR", URLs limpas, mobile-first, HTTPS (Netlify/Vercel)

### 6.2 On-page
- title + meta description com palavra-chave — ✅ v1 tem
- Open Graph + Twitter Card — ✅ v1 tem (falta URL absoluta na og:image)
- alt em toda imagem — ✅ v1 tem

### 6.3 Schema JSON-LD — ✅ feito (2026-07-04)
- `ProfessionalService` (nome, base RJ, areaServed Brasil, WhatsApp, serviços)
- `FAQPage` (6 perguntas da seção FAQ)

### 6.4 Palavras-chave alvo (nacional)
- "criação de site profissional para empresa"
- "quanto custa um site profissional"
- "Google Meu Negócio para empresa"
- "como aparecer no Google" / "empresa não aparece no Google"
- Obs.: alvo nacional = mais concorrência. Blog (6.5) vira ainda mais
  importante pra rankear. GMB da JEMAC continua ancorado no RJ (regra do Google).

### 6.5 Conteúdo contínuo (motor de ranqueamento)
- Blog no site; artigos mirando 1 palavra-chave cada:
  - "Por que minha empresa não aparece no Google?"
  - "Quanto custa um site que rankeia?"
  - "SEO local: como aparecer no mapa do Google"
- Esteira: `/seo` → `/publicar-tema` → `/aprovar-post`

### 6.6 Pós-deploy
- Google Search Console + GA4
- Google Business Profile da JEMAC
- Monitoramento via `/seo` e `/relatorio-ads`

---

## 7. Técnica / performance

- **Trocar Tailwind CDN por CSS compilado/estático** — CDN é dev-only,
  pesa e derruba Core Web Vitals. Meta: carregar < 1s.
- Mobile first: 83% do tráfego de landing page é mobile e converte
  40-51% pior quando mal otimizado. Testar tudo no celular.
- Imagens: webp, tamanhos certos (já ok — passaro-hero 512px, web 800px)
- Deploy: GitHub + Netlify/Vercel via `/salvar`

---

## 8. Fases de execução

1. **Fase 1 — conversão:** ✅ feita (2026-07-04) — Portfólio, Por que a
   JEMAC, FAQ, micro-sinais no hero, schema JSON-LD
2. **Fase 2 — SEO técnico:** sitemap, robots, Tailwind estático,
   og:image absoluta (precisa do domínio/URL final)
3. **Fase 3 — publicar:** deploy Netlify/Vercel + Search Console +
   GA4 + GMB da JEMAC
4. **Fase 4 — movimento:** animação do pássaro em 2 versões
   (leve SVG/CSS vs. rica estilo Noomo) — dono escolhe
5. **Fase 5 — conteúdo contínuo:** blog via esteira `/publicar-tema`

---

## 9. Decisões abertas

- [ ] Animação do pássaro: leve (SVG/CSS) ou pesada (WebGL estilo Noomo)
- [ ] Hospedagem: Netlify ou Vercel (nenhuma conta confirmada ainda)
- [ ] Domínio próprio (jemac.com.br?) — necessário pra SEO sério
- [x] Case real pro portfólio: Um Lugar Encantado — https://umlugarencantado.netlify.app/
      (decoração de festas, Grande SP; destacar o trabalho, não a localização)
- [ ] Mais 1-2 cases futuros (opcional: projetos-estudo enquanto não vêm)
- [x] Serviços, cidade, contato, preço — definidos (ver empresa.md)
- [x] Escopo v1 fatiado — construído

---

## 10. Referências de pesquisa (2026)

- CTA acima da dobra obrigatório; formulário curto; 1 objetivo por página
  — https://gabrieldosite.com.br/landing-page-para-2026-template-checklist-de-conversao/
- Prova social (depoimentos, prints WhatsApp, Google Reviews) = confiança
  — https://blog.greatpages.com.br/post/40-exemplos-landing-pages-que-mais-convertem-2026
- Trust signals acima da dobra: +20-40% conversão
  — https://www.saashero.net/design/landing-page-design-trust-signals/
- Remover navegação dobra conversão; headline <10 palavras
  — https://shalev.agency/blog/landing-page-design-best-practices
- Mobile: 83% do tráfego, converte 40-51% pior se mal feito
  — https://www.uforocks.com/blog/landing-page-design-best-practices/
