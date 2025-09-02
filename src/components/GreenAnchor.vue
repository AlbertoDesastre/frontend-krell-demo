<template>
  <a class="special-anchor" :href="props.url" :target="blank ? '_blank' : ''"
    >{{ props.text }}<span>^</span></a
  >
</template>
<script setup lang="ts">
const props = defineProps<{ text: string; url: string; blank?: boolean }>()
</script>

<style lang="css" scoped>
/* BOTÓN VERDE QUE REDIRIGE A OTROS SITIOS */
.special-anchor {
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  text-decoration: none;
}

.special-anchor,
.special-anchor span {
  font-size: 20px;
  font-weight: 800;
  color: var(--green-lime);
}

.special-anchor span {
  font-size: 25px;
  transform: rotate(90deg);
  transition: all 0.2s ease;
}

.special-anchor:hover span {
  transform: rotate(90deg) translateY(-6px);
}
</style>
