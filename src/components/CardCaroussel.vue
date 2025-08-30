<template>
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
</template>

<script setup lang="ts">
export type CardImage = {
  src: string
  text: string
}

const props = defineProps<{ imgs: CardImage[] }>()
</script>

<style scoped>
.card-list {
  display: flex;
  gap: 20px;
  animation: scroll 70s linear infinite;
}

.card-caroussel:hover .card-list {
  animation-play-state: paused;
}

@keyframes scroll {
  to {
    transform: translateX(-100%);
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
