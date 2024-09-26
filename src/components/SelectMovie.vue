<script setup>
import { ref, defineProps } from 'vue'
import FormRandom from './FormRandom.vue'
import RuletaRandom from './RuletaRandom.vue'

const typeSelectMovie = ref('ruleta')

const props = defineProps({
  items: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <div class="btn-group" role="group" aria-label="Basic radio toggle button group">
    <input
      type="radio"
      class="btn-check"
      name="btnradio"
      id="btnradio1"
      autocomplete="off"
      checked
      value="ruleta"
      v-model="typeSelectMovie"
    />
    <label class="btn btn-outline-primary" for="btnradio1">Ruleta</label>

    <input
      type="radio"
      class="btn-check"
      name="btnradio"
      id="btnradio3"
      autocomplete="off"
      value="formulario"
      v-model="typeSelectMovie"
    />
    <label class="btn btn-outline-primary" for="btnradio3">Formulario</label>
  </div>

  <FormRandom v-if="typeSelectMovie === 'formulario'" />
  <RuletaRandom v-else :items="props.items" />
</template>

<style scoped>
.btn-group {
  margin: 0 auto;
  text-align: center;
  margin-bottom: 30px;
}

.btn-outline-primary {
  --bs-btn-font-weight: 600;
  --bs-btn-color: var(--kuromi-purple);
  --bs-btn-bg: transparent;
  --bs-btn-border-color: var(--kuromi-purple);
  --bs-btn-hover-color: var(--kuromi-white);
  --bs-btn-hover-bg: var(--kuromi-purple); /* Morado más claro para hover */
  --bs-btn-hover-border-color: var(--kuromi-purple); /* Morado más claro para hover */
  --bs-btn-focus-shadow-rgb: var(--kuromi-purple); /* Sombra de enfoque con morado */
  --bs-btn-active-color: var(--bs-btn-hover-color);
  --bs-btn-active-bg: var(--kuromi-purple); /* Mantiene el morado brillante al presionar */
  --bs-btn-active-border-color: var(--kuromi-hover); /* Morado más claro para borde activo */
}
</style>
