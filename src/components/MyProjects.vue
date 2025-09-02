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

    <article>
      <ProjectCard />
    </article>
  </section>
</template>

<script setup lang="ts">
import ProjectCard from './ProjectCard.vue'
</script>

<style scoped>
.projects-display-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: hidden;

  max-width: 900px;
  margin: 20px auto;
}
</style>
