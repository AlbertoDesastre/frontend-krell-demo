<template>
  <!-- Presentación -->
  <h1>ALBERTO ARMAS</h1>
  <h2>FULL-STACK DEVELOPER</h2>
  <h3>(React/Vue + Nest.js/Node)</h3>

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
        <h2>Sobre mí</h2>
        <p>
          Soy desarrollador y analista orientado a producto. Me muevo bien entre negocio y código:
          traduzco requisitos en soluciones reales y escalables acompañadas de
          <strong>pruebas automatizadas y código limpio.</strong>
        </p>

        <ul class="bullets">
          <li>
            Último rol:
            <strong>Developer & Functional Analyst / PM en Thalamus</strong>(eCommerce/CRM).
          </li>
          <li>
            Inglés profesional; trabajo con equipos de
            <strong>Bulgaria, Lituania, Austria</strong>, etc.
          </li>
          <li>
            Mentalidad <strong> clean code, SOLID, arquitectura hexagonal </strong>y foco en
            entregar valor.
          </li>
        </ul>

        <p>
          <strong>Si quieres trabajar conmigo te interesa saber que...</strong>
        </p>
        <ul class="bullets">
          <li>
            Soy una mezcla de <strong>BA/PM + Dev</strong> → menos fricción entre negocio y equipo
            técnico.
          </li>
          <li>Me gusta el <strong>Testing</strong> (unitarias, integración y E2E).</li>
          <li>
            Tengo <strong>autonomía</strong> y comunicación clara; acostumbrado a entornos
            exigentes.
          </li>
        </ul>
      </div>

      <article class="redirections">
        <GreenAnchor :url="''" :text="'MI EXPERIENCIA'" />
        <GreenAnchor :url="''" :text="'MI STACK'" />
        <GreenAnchor :url="''" :text="'MIS PROYECTOS'" />
      </article>
    </article>
  </section>

  <StackDisplay />

  <MyProjects />
</template>

<script setup lang="ts">
/* componentes */
import GreenAnchor from '@/components/GreenAnchor.vue'
import MyProjects from '@/components/MyProjects.vue'
import SocialMedia from '@/components/SocialMedia.vue'
import StackDisplay from '@/components/StackDisplay.vue'
/* imagenes */
import me from '@/imgs/me.webp'
</script>

<style scoped>
/* Textos*/
h1,
h2,
h3 {
  text-align: center;
}

h1 {
  font-weight: 100;
}

h2 {
  font-weight: 500;
}

h3 {
  font-weight: 100;
  font-size: 1.2rem;
}

li {
  font-size: 18px;
}

strong {
  font-weight: 600;
}

/* Presentación con texto */
.presentation-and-description-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.bullets {
  margin-top: 12px;
  margin-left: 40px;
  list-style: circle;
}

.presentation {
  margin-left: 10px;
  width: 560px;
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

.redirections {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
}

/* Stack tecnológico */
.stack-display-container {
  max-width: 900px;
  margin: 20px auto;
}
</style>
