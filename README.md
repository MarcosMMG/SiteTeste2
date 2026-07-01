# JEMAC — Site & Presença Digital

> Workspace da JEMAC. Missão atual: **construir o site/portfólio storytelling
> da JEMAC** e a camada de SEO que leva o negócio ao topo do Google.

A JEMAC cria sites e portfólios para empresas e melhora a visibilidade
delas na internet (SEO). Este repositório é a operação por trás disso —
e o primeiro projeto rodando aqui é o **próprio site da JEMAC**.

Metáfora da marca: o beija-flor origami subindo — o cliente sai da
invisibilidade e chega ao topo do Google.

---

## O projeto: site da JEMAC

Site estático de storytelling guiado por scroll (referência:
[storytelling.noomoagency.com](https://storytelling.noomoagency.com/)),
com narrativa em 3 atos — **dor** (invisível no Google) → **jornada**
(site + SEO) → **topo** (1º lugar). Construído pra ranquear: HTML
semântico, performance, schema e conteúdo.

**Plano completo:** [`_memoria/plano-site.md`](_memoria/plano-site.md)
— conceito, seções, stack, camada de SEO e fases de execução.

**Status:** planejamento. Antes de codar, resolver os bloqueadores
(conteúdo real, cidade-alvo, captação de lead, peso da animação) —
registrados em [`_memoria/estrategia.md`](_memoria/estrategia.md).

---

## Estrutura

`_memoria/` — o cérebro do negócio (empresa, preferências, estratégia,
plano do site). O Claude lê antes de cada resposta.

`identidade/` — o rosto da marca (logos, beija-flor origami, favicon,
paleta). Detalhes em [`identidade/design-guide.md`](identidade/design-guide.md).
Todo visual respeita isso.

`marketing/`, `saidas/`, `scripts/`, `dados/` — produção e resultados,
versionados no GitHub.

`site/` — o site em si (criado na fase de execução).

---

## Como isso roda

Este workspace opera sobre o **JemacPRO** — sistema de skills dentro do
Claude Code. Os comandos que tocam o dia a dia:

- **`/atualizar`** — varre o projeto e reconcilia a memória
- **`/salvar`** — commit + push no GitHub
- **`/seo`** — estratégia de SEO (demanda, concorrência, GMB, ads, GEO)
- **`seo-tecnico`** — SEO de engenharia (schema, Core Web Vitals, sitemap)
- **`/carrossel`, `/publicar-tema`, `/aprovar-post`** — conteúdo pras redes

O projeto também empacota skills de design, dev, motion e marketing
(UI/UX, Motion, frontend, brand) pra construir e animar o site.

---

## Base

Construído sobre o [JemacPRO](https://github.com/MarcosMMG/JemacPRO.git).
A base é o sistema operacional; este repositório é a JEMAC usando ele
pra fazer o próprio site.
