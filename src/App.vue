<script setup>
import StreamSurpriseScreen from '@/components/StreamSurpriseScreen.vue'
import { defineAsyncComponent } from 'vue'

const HomeApp = defineAsyncComponent(() => {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(import('@/components/HomeApp.vue'))
    }, 3000)
  })
})
</script>

<template>
  <Suspense>
    <template #default>
      <HomeApp />
    </template>
    <template #fallback>
      <StreamSurpriseScreen />
    </template>
  </Suspense>
</template>

<style scoped></style>
