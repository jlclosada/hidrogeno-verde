// pages/damas/[id].vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">Detalles de {{ dama.name }}</h2>
    <div class="text-center">
      <img :src="dama.image" :alt="`Imagen de ${dama.name}`" class="rounded shadow mb-4 mx-auto w-48 h-48 object-cover" />
    </div>
    <p class="text-gray-700">Edad: {{ dama.age }}</p>
    <p class="text-gray-700">Equipo: {{ dama.equipo }}</p>
    <p class="text-gray-700">Descripción: {{ dama.description }}</p>
    <div class="flex justify-center mt-6">
      <nuxt-link :to="`/damas/${previousDama}`" v-if="previousDama" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600 mx-4">Anterior</nuxt-link>
      <nuxt-link :to="`/damas/${nextDama}`" v-if="nextDama" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">Siguiente</nuxt-link>
    </div>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router';
import { computed } from 'vue';

const route = useRoute();
const damas = [
  { id: 1, name: 'Valle', age: 29, equipo: 'Sevilla', description: 'Fanático de los deportes y la tecnología.', image: 'https://via.placeholder.com/150' },
  { id: 2, name: 'Alejandra', age: 43, equipo: 'Real de Madrid', description: 'Le encanta la música clásica y tocar guitarra.', image: 'https://via.placeholder.com/150' }
];

const dama = computed(() => damas.find(n => n.id === parseInt(route.params.id)));
const currentIndex = computed(() => damas.findIndex(n => n.id === parseInt(route.params.id)));
const previousDama = computed(() => (currentIndex.value > 0 ? damas[currentIndex.value - 1].id : null));
const nextDama = computed(() => (currentIndex.value < damas.length - 1 ? damas[currentIndex.value + 1].id : null));
</script>

<style scoped>
img {
  max-width: 100%;
  height: auto;
}
</style>