# Catalogo de Skills

Skills externas prontas pra instalar. Use como referencia ao criar skills novas com `/mapear-rotinas` ou instale diretamente as que fizerem sentido pro seu negocio.

> Skills globais ficam em `~/.claude/skills/` e funcionam em qualquer projeto.
> Skills locais ficam em `.claude/commands/` e so funcionam nesse projeto.

---

## Escrever copy e textos de venda

### Schwartz Copy (resposta direta)
**O que faz:** Escreve copy de vendas usando a metodologia de Eugene Schwartz (Breakthrough Advertising). Diagnostica o nivel de consciencia e sofisticacao do mercado antes de gerar qualquer texto.
**Bom pra:** Landing pages, emails de venda, VSLs, cartas de venda, paginas de captura
**Como instalar:** Ja vem como skill global. Chamar com `/schwartz-copy`
**Fonte:** Skill validada pelo JemacPRO

### Ogilvy Copy (marca e posicionamento)
**O que faz:** Gera copy institucional usando a metodologia de David Ogilvy. Pesquisa profunda, big idea, headlines informativas.
**Bom pra:** Manifestos de marca, campanhas institucionais, taglines, brand voice, posicionamento
**Como instalar:** Ja vem como skill global. Chamar com `/ogilvy-copy`
**Fonte:** Skill validada pelo JemacPRO

---

## Criar interfaces e paginas web

### UI/UX Pro Max
**O que faz:** Inteligencia de design de UI/UX completa: 67 estilos visuais, 161 paletas de cor, 57 combinacoes de fontes, 25 tipos de grafico, 21 stacks suportadas (React, Next.js, Vue, Svelte, Astro, SwiftUI, React Native, Flutter, etc). Planeja, constroi, revisa e melhora interfaces.
**Bom pra:** Dashboards, landing pages, paineis admin, e-commerce, apps SaaS, qualquer tela que precise de decisao de design (cor, tipografia, layout, acessibilidade)
**Como instalar:** Skill global, ja instalada. Aciona automaticamente em tarefas de UI/UX ou pode ser chamada direto
**Fonte:** Skill global instalada no PC

### Motion
**O que faz:** Cobre a biblioteca Motion (ex-Framer Motion) pra animacoes web: fade-ins, transicoes entre paginas/componentes, gestos de arraste, efeitos de scroll, animacoes de layout. Cobre API vanilla JS e API React.
**Bom pra:** Deixar interfaces com transicoes suaves, animar entrada de elementos, interacoes de gesto
**Como instalar:** Skill global, ja instalada. Aciona ao pedir "anima isso", "transicao suave", "fade in"
**Fonte:** Skill global instalada no PC

### Frontend Design
**O que faz:** Cria interfaces web completas com design de alta qualidade. Gera codigo HTML/CSS/React pronto pra usar, com visual profissional que foge da estetica generica de IA.
**Bom pra:** Landing pages, dashboards, componentes web, paginas de produto
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/frontend-design`
**Fonte:** Skill nativa do Claude Code

---

## Criar visuais e arte

### Canvas Design
**O que faz:** Cria arte visual em PNG e PDF usando principios de design. Posters, capas, pecas graficas.
**Bom pra:** Capas de ebook, banners, pecas visuais, thumbnails
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/canvas-design`
**Fonte:** Skill nativa do Claude Code

---

## Trabalhar com documentos

### PDF
**O que faz:** Manipula PDFs: extrai texto e tabelas, cria novos, junta/separa documentos, preenche formularios.
**Bom pra:** Extrair dados de contratos, criar relatorios em PDF, preencher formularios
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/pdf`
**Fonte:** Skill nativa do Claude Code

### DOCX
**O que faz:** Cria e edita documentos Word com formatacao, tracked changes e comentarios.
**Bom pra:** Propostas formais, contratos, documentos pra clientes que pedem Word
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/docx`
**Fonte:** Skill nativa do Claude Code

### PPTX
**O que faz:** Cria e edita apresentacoes PowerPoint com layouts, speaker notes e formatacao.
**Bom pra:** Apresentacoes pra clientes, decks de vendas, materiais de treinamento
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/pptx`
**Fonte:** Skill nativa do Claude Code

### XLSX
**O que faz:** Cria e edita planilhas com formulas, formatacao e graficos.
**Bom pra:** Relatorios financeiros, dashboards em planilha, analise de dados
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/xlsx`
**Fonte:** Skill nativa do Claude Code

---

## Escrever documentos e specs

### Doc Co-Authoring
**O que faz:** Fluxo guiado pra coescrever documentos. Te entrevista, itera rascunhos, e valida que o documento funciona pro leitor.
**Bom pra:** Propostas tecnicas, specs, documentos de decisao, SOPs
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/doc-coauthoring`
**Fonte:** Skill nativa do Claude Code

---

## Extrair transcricao de video

### YT Transcript
**O que faz:** Extrai transcricoes de videos do YouTube usando yt-dlp. Suporta multiplos idiomas.
**Bom pra:** Criar conteudo a partir de videos (carrosseis, newsletters, posts)
**Precisa de:** yt-dlp instalado (`brew install yt-dlp`)
**Como instalar:** Ja vem como skill global. Chamar com `/yt-transcript`
**Fonte:** Skill validada pelo JemacPRO

---

## Testar sites e apps

### Webapp Testing
**O que faz:** Testa aplicacoes web locais usando Playwright. Captura screenshots, verifica funcionalidade, le logs do browser.
**Bom pra:** Testar landing pages antes de publicar, verificar se tudo funciona em diferentes tamanhos
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/webapp-testing`
**Fonte:** Skill nativa do Claude Code

---

## Criar skills novas

### Skill Creator
**O que faz:** Guia pra criar skills novas do zero. Ajuda a estruturar, definir triggers, e testar.
**Bom pra:** Quando o `/mapear-rotinas` nao cobre o que voce precisa e quer criar algo mais complexo
**Como instalar:** Ja vem nativo no Claude Code. Chamar com `/skill-creator`
**Fonte:** Skill nativa do Claude Code

---

## Como adicionar skills novas a este catalogo

Se voce testou uma skill e quer adicionar aqui pra referencia futura:

```markdown
### Nome da Skill
**O que faz:** [descricao em uma frase]
**Bom pra:** [casos de uso praticos]
**Como instalar:** [comando ou instrucao]
**Fonte:** [de onde veio — skill nativa, criada por voce, ou de terceiros]
```
