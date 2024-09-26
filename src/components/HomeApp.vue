<script setup>
import { onMounted, ref } from 'vue'
import LayoutApp from '@/layouts/LayoutApp.vue'
import NavBar from './NavBar.vue'
import CarouselStream from './CarouselStream.vue'
import SelectMovie from './SelectMovie.vue'

const API_URL = import.meta.env.VITE_APP_API_URL
const items = ref(null)

const fetchData = async () => {
  try {
    const response = await fetch(API_URL)
    if (!response.ok) {
      throw new Error(`HTTP error! Status: ${response.status}`)
    }
    const data = await response.json()
    items.value = data.data
  } catch (error) {
    console.error('Error fetching data:', error)
  }
}

onMounted(() => {
  fetchData()
})
</script>

<template>
  <LayoutApp>
    <template #navbar>
      <NavBar />
    </template>
    <template #carousel-img>
      <CarouselStream :items="items" />
    </template>
    <template #select-movie>
      <SelectMovie :items="items" />
    </template>
    <template #card-movie-selected>Mi PELICULA/SERIE</template>
    <template #footer>By Juan</template>
  </LayoutApp>
</template>
