---
name: motion
description: Use this skill whenever the user wants to add animations to a website or web app — fade-ins, transitions between pages/components, drag/gesture interactions, scroll-triggered effects, or layout animations. Covers the "motion" library (formerly Framer Motion, github.com/motiondivision/motion), including installation, the vanilla JS API (motion package) vs the React API (motion/react), core patterns (animate, AnimatePresence, variants, gestures, scroll animations), and when to pick one API over the other. Trigger this even if the user just says "animate this", "make it fade in", "add a transition", "smooth this interaction", without naming the library explicitly.
---

# Motion (ex-Framer Motion)

Lib de animação JS/React. Repo: https://github.com/motiondivision/motion

## Instalação

React project (Next.js, Vite+React, CRA):
```bash
npm install motion
```
Import: `import { motion, AnimatePresence } from "motion/react"`

Site sem framework (HTML puro/vanilla JS):
```bash
npm install motion
```
Import: `import { animate, scroll, inView } from "motion"`

Sem build tool (script tag direto):
```html
<script type="module">
  import { animate } from "https://cdn.jsdelivr.net/npm/motion@latest/+esm";
</script>
```

## Quando usar qual API

- Projeto React/Next/Remix → `motion/react`. Componentes `<motion.div>` substituem elementos normais, ganham props de animação.
- HTML/JS puro, sem framework → `motion` (vanilla). Funções `animate()`, `scroll()`, `inView()` direto no DOM.
- Não misturar as duas em um mesmo projeto sem motivo — vanilla é mais leve, React API tem mais conveniências (AnimatePresence, variants, layout animations automáticas).

## Padrões básicos — motion/react

### animate simples
```jsx
import { motion } from "motion/react"

<motion.div
  initial={{ opacity: 0, y: 20 }}
  animate={{ opacity: 1, y: 0 }}
  transition={{ duration: 0.5 }}
/>
```

### Gestures (hover, tap, drag)
```jsx
<motion.button
  whileHover={{ scale: 1.05 }}
  whileTap={{ scale: 0.95 }}
/>

<motion.div drag dragConstraints={{ left: 0, right: 300 }} />
```

### Variants (estados nomeados, reutilizáveis)
```jsx
const variants = {
  hidden: { opacity: 0, y: 20 },
  visible: { opacity: 1, y: 0 },
}

<motion.div variants={variants} initial="hidden" animate="visible" />
```
Útil pra orquestrar filhos: pai com `variants` + `staggerChildren`, filhos com `variants` próprios sem precisar repetir `initial`/`animate`.

### AnimatePresence (entrada/saída ao desmontar)
```jsx
import { AnimatePresence, motion } from "motion/react"

<AnimatePresence>
  {isVisible && (
    <motion.div
      key="box"
      initial={{ opacity: 0 }}
      animate={{ opacity: 1 }}
      exit={{ opacity: 0 }}
    />
  )}
</AnimatePresence>
```
Necessário pra animar saída — sem isso o elemento some instantâneo no unmount. Cada filho direto precisa de `key` única.

### Scroll-triggered (entra na viewport)
```jsx
<motion.div
  initial={{ opacity: 0 }}
  whileInView={{ opacity: 1 }}
  viewport={{ once: true }}
/>
```

### Scroll-linked (progresso vinculado ao scroll)
```jsx
import { useScroll, useTransform, motion } from "motion/react"

const { scrollYProgress } = useScroll()
const scale = useTransform(scrollYProgress, [0, 1], [1, 2])

<motion.div style={{ scale }} />
```

## Padrões básicos — vanilla motion

### animate direto no DOM
```js
import { animate } from "motion"

animate("#box", { opacity: 1, y: 0 }, { duration: 0.5 })
```

### Scroll
```js
import { scroll, animate } from "motion"

scroll(animate("#box", { scale: [0, 1] }))
```

### Elemento entra na viewport
```js
import { inView, animate } from "motion"

inView("#box", (info) => {
  animate(info.target, { opacity: 1 })
})
```

## Armadilhas comuns

- Esquecer `key` única nos filhos do `AnimatePresence` → exit animation não dispara.
- Animar `layout` (`layout` prop) e mexer em CSS Grid/Flexbox que muda dimensões fora do React → pode gerar flicker. Usar `LayoutGroup` quando tiver vários elementos com layout animado relacionados.
- Em Next.js App Router, `motion/react` exige client component (`"use client"` no topo do arquivo) — `motion.div` usa hooks internamente.
- `whileInView` dispara toda vez que entra/sai da viewport por padrão; usar `viewport={{ once: true }}` se quiser só uma vez.
