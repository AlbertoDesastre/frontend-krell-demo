<template>
  <section class="shadow-wrapper">
    <section class="card-caroussel">
      <ul class="card-list">
        <li class="card" v-for="img in props.imgs" :key="img.src">
          <img :src="img.src" />
          <span>{{ img.text }}</span>
        </li>

        <li class="card replica" v-for="img in props.imgs" :key="img.src">
          <img :src="img.src" />
          <span>{{ img.text }}</span>
        </li>

        <li class="card replica" v-for="img in props.imgs" :key="img.src">
          <img :src="img.src" />
          <span>{{ img.text }}</span>
        </li>

        <li class="card replica" v-for="img in props.imgs" :key="img.src">
          <img :src="img.src" />
          <span>{{ img.text }}</span>
        </li>
      </ul>
    </section>
  </section>
</template>

<script setup lang="ts">
export type CardImage = {
  src: string
  text: string
}

const props = defineProps<{ imgs: CardImage[] }>()
</script>

<style scoped>
.shadow-wrapper {
  max-width: 900px;
  position: relative;
}

.shadow-wrapper::before,
.shadow-wrapper::after {
  content: '';
  position: absolute;
  top: 0;
  width: 60px;
  height: 100%;
  z-index: 2;
}

.shadow-wrapper::before {
  background: linear-gradient(to right, var(--background-black) 10%, transparent);
}

.shadow-wrapper::after {
  right: 0;
  background: linear-gradient(to left, var(--background-black) 10%, transparent);
}

.card-list {
  display: flex;
  gap: 20px;
  animation: scroll 110s linear infinite;
}

.card-caroussel:hover .card-list {
  animation-play-state: paused;
}

@keyframes scroll {
  to {
    transform: translateX(
      -1000%
    ); /* En realidad esto más los segundos de animación en card-list es lo que aumenta la velocidad. */
  }
}

.card {
  width: 100px;
  padding: 10px;
}

.card img {
  width: 80px;
  display: block;
  margin: 0 auto;
  filter: grayscale(20%);
}

.card span {
  display: block;
  text-align: center;
  margin: 10px 0;
}
</style>
