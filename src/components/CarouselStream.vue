<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  items: Array
})
</script>

<template>
  <h1 class="carousel-title">Explora nuestras películas y series recomendadas</h1>

  <div id="carouselExampleFade" class="carousel slide carousel-fade" data-bs-ride="carousel">
    <!-- Imágenes dinámicas con v-for -->
    <div class="carousel-inner">
      <div
        v-for="(item, index) in props.items"
        :key="index"
        :class="['carousel-item', { active: index === 0 }]"
      >
        <img :src="item.scr" class="d-block w-100" :alt="item.nombre" loading="lazy" />
        <div class="carousel-caption d-none d-md-block">
          <h5>{{ item.nombre }}</h5>
          <p>{{ item.tipo }} - IMDb: {{ item.imdb }}</p>
        </div>
      </div>
    </div>

    <!-- Controles del carousel -->
    <button
      class="carousel-control-prev"
      type="button"
      data-bs-target="#carouselExampleFade"
      data-bs-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button
      class="carousel-control-next"
      type="button"
      data-bs-target="#carouselExampleFade"
      data-bs-slide="next"
    >
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<style scoped>
.carousel-title {
  margin-bottom: 56px;
  text-align: center;
  font-size: 2rem;
}
</style>
