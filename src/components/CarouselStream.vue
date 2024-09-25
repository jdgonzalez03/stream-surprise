<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  items: Array
})
</script>

<template>
  <h1 class="carousel-title">Explora nuestras películas y series <span>recomendadas.</span></h1>

  <!-- TODO: Add loading status while image is loading -->
  <div id="carouselExampleFade" class="carousel slide carousel-fade" data-bs-ride="carousel">
    <!-- Imágenes dinámicas con v-for -->
    <div class="carousel-inner">
      <div
        v-for="(item, index) in props.items"
        :key="index"
        :class="['carousel-item', { active: index === 0 }]"
      >
        <img :src="item.scr" class="d-block w-100" :alt="item.nombre" loading="lazy" />
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
  margin: 0 0 24px;
  text-align: center;
  font-size: 2rem;
  font-weight: bold;
  color: var(--kuromi-white);
  text-transform: uppercase;
  letter-spacing: 1px;
  animation: fadeInDown 1s ease-out;
}

.carousel-title span {
  color: var(--kuromi-purple);
  padding-left: 5px;
  box-shadow: 0 12px 12px -9px var(--kuromi-hover);
}

@keyframes fadeInDown {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.carousel {
  height: 600px;
}

.carousel-item img {
  aspect-ratio: auto;
  max-height: 600px;
  object-fit: cover;
  object-position: center;
  transition: transform 0.5s ease-in-out;
}

.carousel-item img:hover {
  transform: scale(1.15);
}

/*TODO: Add media querys to differents screen's sizes*/
</style>
