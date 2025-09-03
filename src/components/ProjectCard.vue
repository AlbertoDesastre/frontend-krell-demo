<template>
  <section :id="props.id" class="project-card">
    <article class="description">
      <h3>{{ props.type }}</h3>
      <h2>{{ props.name }}</h2>

      <p>
        {{ props.text }}
      </p>

      <div class="anchors">
        <GreenAnchor url="" text="Ver código" />
        <GreenAnchor url="" text="Ver repositorio" />
      </div>
    </article>

    <article class="thumbnail">
      <img :src="props.img" />
      <article class="technologies">
        <span v-for="tech in technologies" :key="tech"> {{ tech }}</span>
      </article>
    </article>
  </section>
</template>

<script setup lang="ts">
import GreenAnchor from './GreenAnchor.vue'

const props = defineProps<{
  id: string
  type: string
  name: string
  text: string
  img: string
  technologies: string[]
}>()
</script>

<style lang="css" scoped>
.project-card {
  display: flex;
  gap: 20px;
}

h3,
h2 {
  margin-top: 12px;
}

h3 {
  font-weight: 38;
}

h2 {
  font-weight: 300;
}

.description {
  display: flex;
  flex-direction: column;
  height: 400px;
  width: 500px;
}

.description p {
  margin: 20px 0px;
}

.anchors {
  display: flex;
  flex-direction: column;
  margin: auto 0;
}

.thumbnail {
  position: relative;
  max-width: 300px;
}

.thumbnail img {
  width: 100%;
  display: block;
  margin: 12px auto 0 auto;
}

.thumbnail article {
  display: flex;
  flex-wrap: wrap;
}

.technologies {
  width: 100%;
  margin: 0 auto;
}

.technologies span {
  font-size: 12px;
  padding: 6px 8px;
  border-radius: 20px;
  color: rgb(195, 189, 245);
  background-color: rgb(44, 38, 94);
  margin-top: 4px;
  margin-right: 6px;
}
</style>
