# Plano — Site JEMAC (storytelling + SEO)

> Referência visual: https://storytelling.noomoagency.com/
> Status: planejado, ainda NÃO executado. Decisões abertas no fim.

---

## 1. Conceito / narrativa

Metáfora central: **beija-flor origami subindo ao topo** = cliente saindo
da invisibilidade pro 1º lugar no Google. O site conta uma história guiada
por scroll, não é catálogo.

Arco em 3 atos:
- **Dor** → "Sua empresa existe, mas ninguém te acha."
- **Jornada** → o que a JEMAC faz (site + SEO + visibilidade), pássaro ganha altura.
- **Topo** → "Do invisível ao topo do Google." CTA pra contato.

Tom: confiança e segurança (ver `preferencias.md`).

---

## 2. Seções (ordem do scroll)

| # | Seção | Conteúdo | Animação |
|---|-------|----------|----------|
| 1 | Hero | Logo JEMAC + frase de impacto + "role pra explorar" | Beija-flor entra voando, fundo escuro |
| 2 | A dor | "Você tá invisível no Google" | Texto revela no scroll |
| 3 | A virada | O que a JEMAC entrega (sites, SEO, portfólio) | Pássaro sobe conforme scrolla |
| 4 | Como funciona | 3 passos: diagnóstico → site/SEO → topo | Cards em stagger |
| 5 | Portfólio | Grade de projetos (placeholder até ter cases) | Hover reveal |
| 6 | Prova / confiança | Diferencial, garantia | Fade-in |
| 7 | Topo (CTA) | "Chegue ao topo. Fale com a JEMAC." + form/WhatsApp | Pássaro no ponto mais alto, accent laranja |
| 8 | Footer | Contato, redes, logo-branco | — |

---

## 3. Stack técnico

- Estático: HTML + CSS + JS puro (rápido, bom pra SEO)
- Tailwind (CDN) pra estilo
- Motion (motion/GSAP ScrollTrigger) pras animações de scroll
- Deploy: Netlify ou Vercel (grátis, deploy via GitHub — compatível com `/salvar` e `/aprovar-post`)

---

## 4. Design (do design-guide.md)

- Fundo escuro #0D0D0D, texto branco, accent laranja #FF6600
- Tipografia geométrica bold
- logo-branco.png no header, passaro.png como elemento animado
- Cantos retos, sombras sutis, muito respiro

---

## 5. Estrutura de arquivos

```
SiteTeste2/
  site/
    index.html
    css/style.css
    js/scroll.js
    assets/  (logos, passaro, imagens)
```

---

## 6. Camada SEO (objetivo: rankear)

### 6.1 SEO técnico
- HTML semântico (1 H1, hierarquia H2/H3, main/section)
- Site estático = carregamento rápido (Core Web Vitals)
- sitemap.xml + robots.txt
- URLs limpas, lang="pt-BR"
- Mobile-first
- HTTPS (Netlify/Vercel grátis)

### 6.2 On-page (cada página)
- title + meta description com palavra-chave
- Open Graph + Twitter Card
- alt em toda imagem
- Palavra-chave no H1, 1º parágrafo, corpo natural

### 6.3 Schema / JSON-LD
- LocalBusiness / ProfessionalService
- FAQPage na seção de dúvidas
- BreadcrumbList

### 6.4 Conteúdo = motor de ranqueamento
- Blog dentro do site, artigos sobre dores do cliente:
  - "Por que minha empresa não aparece no Google?"
  - "Quanto custa um site que rankeia?"
  - "SEO local: como aparecer no mapa do Google"
- Cada artigo mira 1 palavra-chave
- Esteira com as skills JemacPRO:
  - `/seo` → fluxo 8 passos (demanda, concorrência, GMB, on-page, conteúdo, ads, monitoramento, GEO)
  - `/publicar-tema` → tema → artigo + carrossel + legendas
  - `/aprovar-post` → publica e deploya

### 6.5 Palavras-chave alvo (rascunho — definir cidade/mercado)
- "criação de site para empresa [cidade]"
- "agência de SEO [cidade]"
- "como aparecer no Google"
- "site profissional para pequena empresa"

### 6.6 Pós-deploy (medir)
- Google Search Console
- Google Analytics
- Google Business Profile (GMB) — crítico pra SEO local
- Monitoramento via `/seo` e `/relatorio-ads`

---

## 7. Fases de execução (quando aprovar)

1. Esqueleto — HTML + seções + conteúdo storytelling
2. Estilo — Tailwind + brand, responsivo mobile
3. Movimento — animações de scroll
4. SEO — semântica, meta, schema, sitemap, performance
5. Deploy — GitHub + Netlify/Vercel via `/salvar`
6. Conteúdo contínuo — esteira `/seo` + `/publicar-tema`

---

## 8. Pendências / decisões abertas

- [x] `passaro.png` (ícone sozinho) salvo em identidade/
- [ ] Conteúdo real: serviços exatos, oferta/preço, contato (WhatsApp/email), cases
- [ ] Cidade/mercado alvo (pra palavras-chave de SEO local)
- [ ] Decisão: animação pássaro leve (SVG/CSS) ou pesada (WebGL estilo Noomo)
- [ ] Decisão: v1 página inteira ou Hero+Dor+CTA primeiro
- [ ] Decisão: hospedagem (Netlify/Vercel já existe?)
