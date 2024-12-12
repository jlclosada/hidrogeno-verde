// pages/proyectos.vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">Proyectos</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div v-for="i in 6" :key="i" class="bg-white shadow rounded-lg p-4 transform hover:scale-105 transition">
        <h3 class="font-bold text-lg mb-2">Proyecto {{ i }}</h3>
        <p class="text-gray-700">Descripción del proyecto número {{ i }}.</p>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
</style>

