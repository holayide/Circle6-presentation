---
theme: seriph
# theme: default
background: https://cover.sli.dev
title: Welcome to Slidev
info: |
  ## Slidev Starter Template  
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true

---
<style>
  h1 {
    padding-bottom: .3rem;
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }

  h2 {
    color: #2B90B6;
    margin-bottom: 1.8rem;
    font-family: 'Inter', sans-serif;
  }

  h3 {
    margin-top: 1.3rem;
    color: #2B90B6;
  }

  span {
    font-size: 1rem
  }

  p,li,pre {
    font-family: 'Inter', sans-serif;
    letter-spacing: 0.05em;
  }
</style>

# Welcome to Circle 6 Presentation


<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

---
src: ./src/toc.md 
---

---
src: ./src/dom.md 
---

---
src: ./src/event.md 
---

---
src: ./src/callback.md 
---

---
src: ./src/promise.md 
---

---
src: ./src/api.md 
---

---
src: ./src/modules.md 
---

---
src: ./src/bundlers.md
---

---
src: ./src/intro.md
---

---
src: ./src/react-fundamental.md
---
