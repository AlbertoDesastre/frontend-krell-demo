<template>
  <section class="projects-display-container">
    <article>
      <!-- Texto de presentación -->
      <h3 style="margin-bottom: 20px">Proyectos & Repositorios</h3>

      <p>
        He creado múltiples proyectos que cumplen con los estándares de la industria. Aquí tienes
        una selección de mis mejores trabajos.
      </p>
    </article>

    <article class="project-list">
      <ProjectCard
        v-for="(project, slideIdx) in projects"
        :class="{ active: slideIdx === activeIndex }"
        :key="normalize(project.name)"
        :id="normalize(project.name)"
        :type="project.type"
        :name="project.name"
        :text="project.text"
        :img="project.img"
        :technologies="project.technologies"
      />
    </article>

    <article class="sliders">
      <a
        v-for="(project, slideIdx) in projects"
        :href="'#' + normalize(project.name)"
        class="slider-anchor"
        :key="normalize(project.name)"
        @click="activeIndex = slideIdx"
      >
        <span :class="{ active: slideIdx === activeIndex }"></span>
      </a>
    </article>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

import ProjectCard from './ProjectCard.vue'
import leeer from '@/imgs/leeer-logo.png'
import nest from '@/imgs/nest.js.png'
import vue from '@/imgs/vue.js.png'

type Project = {
  type: string
  name: string
  text: string
  img: string
  technologies: string[]
}
const projects: Project[] = [
  {
    type: 'Backend APP',
    name: 'leeer - API',
    text: 'loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum',
    img: leeer,
    technologies: ['Nest.js', 'Node', 'Typescript', 'MySQL', 'TypeORM', 'Postman', 'Swagger'],
  },
  {
    type: 'Frontend APP',
    name: 'leeer',
    text: 'loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum',
    img: vue,
    technologies: ['Vue', 'Vue Router', 'Pinia', 'Vitest', 'Typescript'],
  },

  {
    type: 'ANOTHER ONE',
    name: 'oneeee',
    text: 'loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum',
    img: nest,
    technologies: ['Vue', 'Vue Router', 'Pinia', 'Vitest', 'Typescript'],
  },
]

const activeIndex = ref(0)

const normalize = (name: string): string => {
  return name.toLowerCase().replace(/\s+/g, '').replace(/-/g, '')
}
</script>

<style scoped>
/* Estilos del contenedor */
.projects-display-container {
  display: flex;
  flex-direction: column;
  align-items: center;

  max-width: 900px;
  margin: 20px auto;
}

.project-list {
  width: 100%;
  display: flex;
  overflow: hidden;
}

/* Adaptaciones a proyectos */
.project-card {
  display: none;
}

.project-card.active {
  display: inherit;
  animation: shake 200ms linear;
}

.project-card.active .thumbnail img {
  animation: shake 20000ms linear;
  animation-iteration-count: 5;
}

@keyframes shake {
  0% {
    transform: rotateZ(1deg) scale(1.1);
  }

  25% {
    transform: rotateZ(-1deg);
  }

  50% {
    transform: rotateZ(1deg);
  }

  75% {
    transform: rotateZ(-1deg);
  }

  100% {
    transform: rotateZ(1deg);
  }
}

@keyframes grow {
  from {
    transform: scale(1);
  }

  to {
    transform: scale(0.9);
  }
}

/* Estilo de los Sliders */
.sliders {
  display: flex;
}

.slider-anchor {
  position: relative;
  width: 10px;
  height: 10px;
  margin: 0 3px;
  z-index: 1;
  cursor: pointer;
}

.slider-anchor span {
  width: 10px;
  height: 10px;

  background-color: gray;
  position: absolute;
  border-radius: 50%;

  transition: all 200ms ease;
}

.slider-anchor span.active {
  width: 15px;
  height: 15px;
  margin-top: -5px;
  margin-left: -3px;
  background-color: #2c265e;
}
</style>
