<template>
  <section class="stack-display-container">
    <!-- Texto de presentación -->
    <p>UN PROBLEMA SÓLO ES UN RETO POR RESOLVER</p>
    <h3 style="margin-bottom: 20px">Stack & Especialidad</h3>

    <p>
      Desde HTML, CSS y JS Vanilla para proyectos pequeños hasta trabajos medianos y grandes con Vue
      y React, con testing unitarios & de integración, interfaces limpias y responsivas.
    </p>

    <p>
      Uso Librerías de Componentes, APIs de terceros y gestores de estado como Pinia, Redux. (¡Hasta
      diseño mis propias APIs con Node/Nest.js!)
    </p>

    <p>
      Visita mi <a><span class="highlight">Linkedin</span></a> para más información.
    </p>

    <!-- Stack tecnológico -->
    <CardCaroussel :imgs />
    <CardCaroussel :imgs :reverse="true" />
  </section>
</template>

<script setup lang="ts">
/* componentes */
import type { CardImage } from './CardCaroussel.vue'
import CardCaroussel from './CardCaroussel.vue'
/* imagenes */
import jslogo from '@/imgs/js.png'
import nest from '@/imgs/nest.js.png'
import css3 from '@/imgs/css3.png'
import git from '@/imgs/git.png'
import github from '@/imgs/github.png'
import html5 from '@/imgs/html5.png'
import jest from '@/imgs/jest.png'
import nodejs from '@/imgs/node.js.png'
import react from '@/imgs/react.png'
import sass from '@/imgs/sass.png'
import swagger from '@/imgs/swagger.png'
import tailwind from '@/imgs/tailwind-css.png'
import typescript from '@/imgs/typescript.png'
import vscode from '@/imgs/visual-studio-code.png'
import vue from '@/imgs/vue.js.png'

const imgs: CardImage[] = [
  { src: jslogo, text: 'Javascript' },
  { src: typescript, text: 'TypeScript' },
  { src: react, text: 'React' },
  { src: vue, text: 'Vue.js' },
  { src: html5, text: 'HTML5' },
  { src: css3, text: 'CSS3' },
  { src: tailwind, text: 'Tailwind' },
  { src: sass, text: 'Sass' },
  { src: jest, text: 'Jest' },
  { src: swagger, text: 'Swagger' },
  { src: git, text: 'Git' },
  { src: github, text: 'GitHub' },
  { src: nodejs, text: 'Node.js' },
  { src: nest, text: 'Nest.js' },
  { src: vscode, text: 'VS Code' },
]

const back = []
const front = []
</script>

<style scoped>
p {
  margin: 6px;
  text-align: center;
}

.stack-display-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: hidden;
}
</style>
