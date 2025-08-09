---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /images/backgroundaframe.png
# some information about your slides (markdown enabled)
title: Construindo experiências de realidade virtual na Web com A-frame
info: |
  A realidade virtual já está ao alcance do navegador — e criar mundos imersivos nunca foi tão simples. Nesta palestra, vamos explorar o A-Frame, um framework open source baseado em WebVR e WebXR que permite construir experiências 3D e VR usando apenas HTML e JavaScript.
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
seoMeta:
  # By default, Slidev will use ./og-image.png if it exists,
  # or generate one from the first slide if not found.
  ogImage: auto
  # ogImage: https://cover.sli.dev
---

# Construindo experiências de realidade virtual na Web<br>com A-frame

Felipe Do E. Santo

---
transition: fade-out
---

# Quem sou eu?

Head de Tecnologia na Proz Educação e Professor na Fatec Indaiatuba

- 🌐 **Desenvolvedor Web** - desde 2006
- 🦊 **Voluntário da Mozilla** - por quase uma década
- 🎓 **Doutorando em Educação** - pela Unicamp
- 👨‍🎓 **Mestre em Ensino e Processos Formativos** - pela Unesp
- 🎓 **Graduado em Processamento de Dados** - pela Fatec
<br>
<br>

<style>
h1 {
  background-color: #B62B2B;
  background-image: linear-gradient(45deg, #ff6f6fff 10%, #d43737ff 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# A-Frame

A-Frame é um framework web para construção de experiências de realidade virtual (VR) e aumentada (AR) utilizando HTML e JavaScript. Ele abstrai a complexidade do WebVR e WebXR, permitindo que desenvolvedores criem mundos 3D imersivos de forma simples e rápida.

## Exemplo básico

```html [index.html] {all|3|7,13|8-12|8|all}
<html lang="pt-BR">
  <head>
    <script src="https://aframe.io/releases/1.7.0/aframe.min.js"></script>
    <title>Exemplo A-Frame</title>
  </head>
  <body>
    <a-scene>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#ECECEC"></a-sky>
    </a-scene>
  </body>
</html>
```

<style>
h1 {
  background-color: #B62B2B;
  background-image: linear-gradient(45deg, #ff6f6fff 10%, #d43737ff 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Como os objetos funcionam?

Os objetos em A-Frame são representados por entidades (`<a-entity>`), que podem ter componentes e sistemas aplicados a eles. Cada entidade pode ser um objeto 3D, uma câmera, uma luz, entre outros.

## Estrutura básica de uma entidade

```html
<a-entity id="meuObjeto" geometry="primitive: box" material="color: red"></a-entity>
```

- `id`: Identificador único da entidade.
- `geometry`: Define a forma do objeto (neste caso, um cubo).
- `material`: Define a aparência do objeto (neste caso, a cor vermelha).

---
transition: fade-out
---

# Na prática

<iframe 
  src="/exemplo-aframe.html" 
  width="100%" 
  height="400" 
  style="border: none; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);"
  allowfullscreen="true"
  allow="xr"
>
</iframe>

<div class="text-center text-sm mt-2 opacity-75">
  Cena básica em A-Frame renderizando um cubo, uma esfera, um cilindro e um plano
</div>

<style>
h1 {
  background-color: #B62B2B;
  background-image: linear-gradient(45deg, #ff6f6fff 10%, #d43737ff 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: image-right
image: /images/inspector.png
transition: fade-out
---

# A-frame Inspector

Pode ficar mais fácil?

O A-frame Inspector é uma ferramenta poderosa para depuração e visualização de cenas A-Frame. Ele permite que você inspecione e edite entidades em tempo real, visualize componentes e suas propriedades, e muito mais.

Ao pressionar <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>I</kbd><br>(ou <kbd>CMD</kbd> + <kbd>ALT</kbd> + <kbd>I</kbd> no Mac), você pode abrir o Inspector e começar a explorar sua cena.

<style>
h1 {
  background-color: #B62B2B;
  background-image: linear-gradient(45deg, #ff6f6fff 10%, #d43737ff 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Na prática
<br>
<a href="/exemplo-aframe.html" target="_blank" class="text-blue-500 hover:underline">Abrir exemplo em nova janela</a>
<br><br>
Experimente pressionar <kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>I</kbd> para abrir o Inspector

<style>
h1 {
  background-color: #B62B2B;
  background-image: linear-gradient(45deg, #ff6f6fff 10%, #d43737ff 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Quem está usando?

<iframe 
  src="https://aframe.io/showcase/" 
  width="100%" 
  height="450" 
  style="border: none; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);"
  allowfullscreen="true"
  allow="xr"
>
</iframe>

<div class="text-center text-sm mt-2 opacity-75">
  Showcase oficial do A-Frame com diversos exemplos de projetos reais
</div>

<style>
h1 {
  background-color: #B62B2B;
  background-image: linear-gradient(45deg, #ff6f6fff 10%, #d43737ff 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---

# Fique conectado

Como me encontrar?

<div class="flex justify-center items-center gap-12 mt-8">
  <a href="https://www.linkedin.com/in/felipez3r0" target="_blank" class="no-underline hover:scale-110 transition-transform duration-300 flex flex-col items-center">
    <svg xmlns="http://www.w3.org/2000/svg" width="64" height="64" viewBox="0 0 24 24" class="mb-2">
      <path fill="#0A66C2" d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037c-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85c3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065c0-1.138.92-2.063 2.063-2.063c1.14 0 2.064.925 2.064 2.063c0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
    </svg>
    <span class="text-sm">/felipez3r0</span>
  </a>
  
  <a href="https://github.com/felipez3r0" target="_blank" class="no-underline hover:scale-110 transition-transform duration-300 flex flex-col items-center" id="github-icon">
    <svg xmlns="http://www.w3.org/2000/svg" width="64" height="64" viewBox="0 0 24 24" class="mb-2">
      <path fill="currentColor" d="M12 .297c-6.63 0-12 5.373-12 12c0 5.303 3.438 9.8 8.205 11.385c.6.113.82-.258.82-.577c0-.285-.01-1.04-.015-2.04c-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729c1.205.084 1.838 1.236 1.838 1.236c1.07 1.835 2.809 1.305 3.495.998c.108-.776.417-1.305.76-1.605c-2.665-.3-5.466-1.332-5.466-5.93c0-1.31.465-2.38 1.235-3.22c-.135-.303-.54-1.523.105-3.176c0 0 1.005-.322 3.3 1.23c.96-.267 1.98-.399 3-.405c1.02.006 2.04.138 3 .405c2.28-1.552 3.285-1.23 3.285-1.23c.645 1.653.24 2.873.12 3.176c.765.84 1.23 1.91 1.23 3.22c0 4.61-2.805 5.625-5.475 5.92c.42.36.81 1.096.81 2.22c0 1.606-.015 2.896-.015 3.286c0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
    </svg>
    <span class="text-sm">/felipez3r0</span>
  </a>
</div>

<div v-click class="github-slides-pointer">
  <div class="arrow"></div>
  <div class="message">Os slides estão lá!</div>
</div>

<style>
h1 {
  background-color: #B62B2B;
  background-image: linear-gradient(45deg, #ff6f6fff 10%, #d43737ff 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

.github-slides-pointer {
  position: absolute;
  top: 170px;
  right: 200px;
  display: flex;
  align-items: center;
  animation: bounce 1s infinite alternate;
}

.arrow {
  width: 40px;
  height: 20px;
  background: linear-gradient(to bottom right, transparent 50%, #d43737 50%);
  transform: rotate(15deg);
}

.message {
  background-color: #d43737;
  color: white;
  padding: 8px 12px;
  border-radius: 4px;
  font-weight: bold;
  margin-left: -10px;
}

@keyframes bounce {
  from {
    transform: translateY(0);
  }
  to {
    transform: translateY(-10px);
  }
}
</style>

---
transition: fade-out
layout: center
---

# Dúvidas?

<div class="flex flex-col items-center justify-center space-y-6"> 
  <div class="mt-8 text-2xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-red-500 to-orange-500">
    Muito obrigado pela atenção!
  </div>
</div>

<style>
h1 {
  background-color: #B62B2B;
  background-image: linear-gradient(45deg, #ff6f6fff 10%, #d43737ff 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
