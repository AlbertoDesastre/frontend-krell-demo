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
        v-for="project in projects"
        :key="normalize(project.name)"
        :type="project.type"
        :name="project.name"
        :text="project.text"
        :img="project.img"
        :technologies="project.technologies"
      />

      <div class="sliders">
        <a
          :href="'#' + normalize(project.name)"
          class="slider-anchor"
          v-for="project in projects"
          :key="normalize(project.name)"
        >
          <span></span>
        </a>
      </div>
    </article>
  </section>
</template>

<script setup lang="ts">
import ProjectCard from './ProjectCard.vue'
import leeer from '@/imgs/leeer-logo.png'

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
    img: leeer,
    technologies: ['Vue', 'Vue Router', 'Pinia', 'Vitest', 'Typescript'],
  },

  {
    type: 'ANOTHER ONE',
    name: 'oneeee',
    text: 'loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum',
    img: leeer,
    technologies: ['Vue', 'Vue Router', 'Pinia', 'Vitest', 'Typescript'],
  },
]
const normalize = (name: string): string => {
  return name.toLowerCase().replace(/\s+/g, '').replace(/-/g, '')
}
</script>

<style scoped>
.projects-display-container {
  display: flex;
  flex-direction: column;
  align-items: center;

  max-width: 900px;
  margin: 20px auto;
}

.project-list {
  width: 100%;
}

.project-list .project {
  margin: 24px 0;
}

.sliders {
  display: flex;

  gap: 10px;
}

.slider-anchor {
  position: relative;
  width: 40px;
  height: 40px;
  z-index: 1;
  cursor: pointer;
}

.slider-anchor span {
  width: 20px;
  height: 20px;
  background-color: gray;
  position: absolute;
  border-radius: 50%;

  transition: all 200ms ease;
}

.slider-anchor span.active {
  width: 40px;
  height: 40px;
}
</style>
