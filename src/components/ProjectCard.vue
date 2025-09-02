<template>
  <section class="project-card">
    <article>
      <h3>TIPO DE APLICACIÓN</h3>
      <h2>TÍTULO DE LA APLICACIÓN</h2>

      <p><strong>Construido con:</strong> React, Vue, Javascript, SASS.</p>

      <GreenAnchor url="" text="Ver código" />
      <GreenAnchor url="" text="Ver repositorio" />
    </article>

    <article>
      <img :src="nest" />
      <img :src="leeer" />
    </article>
  </section>
</template>

<script setup lang="ts">
import GreenAnchor from './GreenAnchor.vue'

import nest from '@/imgs/nest.js.png'

import leeer from '@/imgs/leeer-logo.png'
</script>
