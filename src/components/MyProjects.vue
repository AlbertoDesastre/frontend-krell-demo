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
        :type="'Backend APP'"
        :name="'leeer - API'"
        :text="'loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum '"
        :img="leeer"
        :technologies="['Nest.js', 'Node', 'Typescript', 'MySQL', 'TypeORM', 'Postman', 'Swagger']"
      />

      <ProjectCard
        :type="'Frontend APP'"
        :name="'leeer'"
        :text="'loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum loremipsum '"
        :img="leeer"
        :technologies="['Vue', 'Vue Router', 'Pinia', 'Vitest', 'Typescript']"
      />
    </article>
  </section>
</template>

<script setup lang="ts">
import ProjectCard from './ProjectCard.vue'
import leeer from '@/imgs/leeer-logo.png'
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
</style>
