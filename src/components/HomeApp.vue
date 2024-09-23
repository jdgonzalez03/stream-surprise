<script setup>
import LayoutApp from '@/components/LayoutApp.vue'
import NavBar from './NavBar.vue'
</script>

<template>
  <LayoutApp>
    <template #navbar>
      <NavBar />
    </template>
    <template #carousel-img>Aquí va mi carousel</template>
    <template #form-random-movie>Mi ruleta y mi formulario</template>
    <template #card-movie-selected>Mi PELICULA/SERIE</template>
    <template #footer>By Juan</template>
  </LayoutApp>
</template>
