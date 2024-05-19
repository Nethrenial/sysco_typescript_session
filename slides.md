---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: https://cover.sli.dev
# some information about your slides, markdown enabled
title: Type Ahead
titleTemplate: "%s - Level up your JS with Powerful Type Safety"
info: |
  Level up your JS with Powerful Type Safety
# apply any unocss classes to the current slide
class: text-center bg-black 
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-up
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
download: true
fonts:
  # basically the text
  sans: Roboto
  # use with `font-serif` css class from UnoCSS
  serif: Roboto Slab
  # for code blocks, inline code, etc.
  mono: Fira Code

export:
  format: pdf
  timeout: 30000
  dark: false
  withClicks: true
  withToc: true

src: ./pages/index.md
---

---
transition: slide-up
src: ./pages/topic-types/index.md
---

---
transition: slide-up
src: ./pages/topic-types/more-examples.md
---

---
transition: slide-up
src: ./pages/topic-interfaces/index.md
---

---
transition: slide-up
src: ./pages/topic-interfaces/more-examples.md
---