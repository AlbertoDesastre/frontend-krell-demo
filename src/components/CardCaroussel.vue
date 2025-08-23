<template>
  <section class="card-caroussel">
    <ul class="card-list">
      <li class="card" v-for="img in props.imgs" :key="img.src">
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
  overflow: scroll;
}

.card {
  width: 200px;
  height: 200px;
  padding: 10px;
}

.card img {
  width: 80px;
  /*  filter: grayscale(100%) brightness(1.25); TODO: Hacer pruebas con este estilo más tarde*/
}

.card span {
  display: inline-block;
  margin: 0px auto;
}
</style>
