// pages/damas/[id].vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">Detalles de {{ dama.name }}</h2>
    <div class="text-center">
      <img :src="dama.image" :alt="`Imagen de ${dama.name}`" class="rounded shadow mb-4 mx-auto w-96 h-96 object-cover hover:scale-105 transition ease-linear" />
    </div>
    <div class="flex flex-col bg-slate-200 mx-auto p-4 rounded shadow-md max-w-2xl text-xl">
      <p class="text-gray-900 font-bold py-2">Edad: <span class="text-gray-700 mx-2">{{ dama.age }}</span></p>
      <p class="text-gray-900 font-bold py-2">Equipo: <span class="text-gray-700 mx-2">{{ dama.equipo }}</span></p>
      <p class="text-gray-900 font-bold py-2">Descripción: <span class="text-gray-700 mx-2">{{ dama.description }}</span></p>
      <p class="text-gray-900 font-bold py-2">¿Gradudado?: <span class="text-gray-700 mx-2">{{ dama.graduado }}</span></p>
    </div>
    <div class="flex justify-center mt-6">
      <nuxt-link :to="`/damas/${previousDama}`" v-if="previousDama" class="bg-pink-400 text-white px-4 py-2 rounded hover:bg-pink-600 mx-4">Anterior</nuxt-link>
      <nuxt-link :to="`/damas/${nextDama}`" v-if="nextDama" class="bg-pink-400 text-white px-4 py-2 rounded hover:bg-pink-600">Siguiente</nuxt-link>
    </div>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router';
import { computed } from 'vue';

import aleImage from '~/assets/images/ale.jpeg';
import valleImage from '~/assets/images/valle.jpeg';

definePageMeta({
  layout: 'damas'
});

const route = useRoute();
const damas = [
  { id: 1, name: 'Valle', age: 29, equipo: 'Sevilla', description: 'Fanático de los deportes y la tecnología.', image: valleImage },
  { id: 2, name: 'Alejandra', age: 43, equipo: 'Real de Madrid', description: 'Le encanta la música clásica y tocar guitarra.', image: aleImage }
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