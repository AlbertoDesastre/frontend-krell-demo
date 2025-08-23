<template>
  <!-- Presentación -->
  <h1>ALBERTO ARMAS</h1>
  <h2>FRONT-END DEVELOPER</h2>

  <section class="presentation-and-description-container">
    <article class="presentation">
      <img :src="me" width="300" heigth="300" />

      <article class="bullet-points">
        <p>Full-Stack developer, con enfoque en Front.</p>
        <p>Graduado en DAW, por la Universidad Alfonso el Sabio X.</p>
        <p>Más de 2 años de experiencia acumulada.</p>
      </article>

      <!-- Mis iconos con Github, Linkdein y el CV -->
      <SocialMedia />
    </article>

    <article class="description">
      <p>
        Me metí en el apasionante mundo de la programación en 2021. ¡Empecé en un bootcamp por
        casualidad y he terminado graduándome de un ciclo DAW!
      </p>
      <p>
        He hecho de todo, desde liderar proyectos como Business Analyst & Project Manager hasta
        diseñar mis propias APIs y crear Fronts personalizados hasta el más mínimo detalle.
      </p>
      <p>
        Tengo el conocimiento y la paciencia necesaria para llevar cualquier proyecto adelante, ¡ya
        sea en Front (mi especialidad) o Back!
      </p>

      <a class="special-anchor">MI EXPERIENCIA <span>^</span></a>
    </article>
  </section>

  <!-- Stack tecnológico -->
  <h3>Stack tecnológico</h3>
  <CardCaroussel :imgs />
</template>

<script setup lang="ts">
/* componentes */
import CardCaroussel, { type CardImage } from '@/components/CardCaroussel.vue'
import SocialMedia from '@/components/SocialMedia.vue'
/* imágenes */
import me from '@/imgs/me.webp'
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
  { src: tailwind, text: 'Tailwind CSS' },
  { src: sass, text: 'Sass' },
  { src: jest, text: 'Jest' },
  { src: swagger, text: 'Swagger' },
  { src: git, text: 'Git' },
  { src: github, text: 'GitHub' },
  { src: nodejs, text: 'Node.js' },
  { src: nest, text: 'Nest.js' },
  { src: vscode, text: 'Visual Studio Code' },
]
</script>

<style scoped>
/* Textos*/
h1,
h2 {
  text-align: center;
}

h1 {
  font-weight: 100;
}

h3 {
  margin: 1rem 0 0.25rem;
}

/* Presentación con texto */
.presentation-and-description-container {
  display: flex;
}

.bullet-points {
  margin-top: 20px;
  margin-bottom: 10px;
}

.presentation,
.bullet-points {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-items: center;
}

.bullet-points p {
  margin: 5px;
  font-weight: 500;
}

/* Descripción */
.presentation,
.description {
  margin-top: 30px;
}

.description {
  max-width: 70ch;
  line-height: 1.35;
}
.description p {
  margin: 0.5rem 0;
}
</style>
