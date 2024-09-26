<script setup>
import { ref, defineProps } from 'vue'
import VueWinwheel from 'vue-winwheel/vue-winwheel.vue'

const props = defineProps({
  items: {
    type: Array,
    Required: true
  }
})

// Configuración de las opciones para la rueda
const options = ref([
  {
    textFillStyle: '#fff',
    fillStyle: '#000',
    text: 'Prize 1'
  },
  {
    textFillStyle: '#000',
    fillStyle: '#fadede',
    text: 'Prize 2'
  },
  {
    textFillStyle: '#fff',
    fillStyle: '#000',
    text: 'Prize 3'
  },
  {
    textFillStyle: '#000',
    fillStyle: '#fadede',
    text: 'Prize 4'
  },
  {
    textFillStyle: '#fff',
    fillStyle: '#000',
    text: 'Prize 5'
  },
  {
    textFillStyle: '#000',
    fillStyle: '#fadede',
    text: 'Prize 6'
  },
  {
    textFillStyle: '#fff',
    fillStyle: '#000',
    text: 'Prize 7'
  },
  {
    textFillStyle: '#000',
    fillStyle: '#fadede',
    text: 'Prize 8'
  }
])
</script>

<template>
  <VueWinwheel :segments="options" />
</template>
