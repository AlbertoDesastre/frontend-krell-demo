<template>
  <!-- Presentación -->
  <h1>ALBERTO ARMAS</h1>
  <h2>FRONT-END DEVELOPER</h2>

  <section class="presentation-and-description-container">
    <article class="presentation">
      <img :src="me" width="300" heigth="300" />

      <article class="bullet-points">
        <p>Full-Stack developer, con <span class="highlight"> enfoque en Front</span>.</p>
        <p>
          <span class="highlight">Graduado en DAW</span>, por la Universidad Alfonso el Sabio X.
        </p>
        <p>Más de <span class="highlight"> 2 años de experiencia</span> acumulada.</p>
      </article>

      <!-- Mis iconos con Github, Linkdein y el CV -->
      <SocialMedia />
    </article>

    <article class="description-container">
      <div class="description">
        <p>
          Me metí en el apasionante mundo de la programación en 2021. ¡Empecé en un bootcamp por
          casualidad y he terminado graduándome de un ciclo DAW!
        </p>
        <p>
          He hecho de todo, desde liderar proyectos como Business Analyst & Project Manager hasta
          diseñar mis propias APIs y crear Fronts personalizados hasta el más mínimo detalle.
        </p>
        <p>
          Tengo el conocimiento y la paciencia necesaria para llevar cualquier proyecto adelante,
          ¡ya sea en Front (mi especialidad) o Back!
        </p>
      </div>

      <article class="redirections">
        <a class="special-anchor">MI EXPERIENCIA <span>^</span></a>
        <a class="special-anchor">MI STACK <span>^</span></a>
        <a class="special-anchor">MIS PROYECTOS <span>^</span></a>
      </article>
    </article>
  </section>

  <StackDisplay />
</template>

<script setup lang="ts">
/* componentes */
import SocialMedia from '@/components/SocialMedia.vue'
import StackDisplay from '@/components/StackDisplay.vue'
/* imagenes */
import me from '@/imgs/me.webp'
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
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.bullet-points {
  margin-top: 20px;
  margin-bottom: 10px;
}

.presentation {
  margin-left: 10px;
  width: 560px;
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

.redirections {
  display: flex;
  flex-direction: column;
}

/* Stack tecnológico */
.stack-display-container {
  max-width: 900px;
  margin: 20px auto;
}
</style>
