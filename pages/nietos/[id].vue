// pages/nietos/[id].vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">Detalles de {{ nieto.name }}</h2>
    <div class="text-center">
      <img :src="nieto.image" :alt="`Imagen de ${nieto.name}`" class="rounded shadow mb-4 mx-auto w-48 h-48 object-cover" />
    </div>
    <p class="text-gray-700">Edad: {{ nieto.age }}</p>
    <p class="text-gray-700">Equipo: {{ nieto.equipo }}</p>
    <p class="text-gray-700">Descripción: {{ nieto.description }}</p>
    <div class="flex justify-center mt-6 mx-6">
      <nuxt-link :to="`/nietos/${previousNieto}`" v-if="previousNieto" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600 mx-4">Anterior</nuxt-link>
      <nuxt-link :to="`/nietos/${nextNieto}`" v-if="nextNieto" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">Siguiente</nuxt-link>
    </div>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router';
import { computed } from 'vue';

import fernandoImage from '~/assets/images/fernando.jpeg';

const route = useRoute();
const nietos = [
  { id: 1, name: 'Fernando', age: 33, equipo: 'Betis', description: 'Fanático de los deportes y la tecnología.', image: fernandoImage },
  { id: 2, name: 'José Luis', age: 29, equipo: 'Sevilla', description: 'Le encanta la música clásica y tocar guitarra.', image: 'https://via.placeholder.com/150' },
  { id: 3, name: 'Kike', age: 29, equipo: 'Betis', description: 'Aficionado a los videojuegos y los cómics.', image: 'https://via.placeholder.com/150' },
  { id: 4, name: 'Pablo', age: 27, equipo: 'Barcelona', description: 'Entusiasta de la cocina y los viajes.', image: 'https://via.placeholder.com/150' },
  { id: 5, name: 'Manuel', age: 29, equipo: 'Vodka', description: 'Amante de las fiestas y el baile.', image: 'https://via.placeholder.com/150' },
  { id: 6, name: 'Javier', age: 29, equipo: 'Sevilla', description: 'Disfruta de la lectura y el senderismo.', image: 'https://via.placeholder.com/150' },
  { id: 7, name: 'Manolo', age: 29, equipo: 'Sevilla', description: 'Apasionado por el cine y la fotografía.', image: 'https://via.placeholder.com/150' },
  { id: 8, name: 'Fran', age: 29, equipo: 'Betis', description: 'Le encanta el diseño gráfico y el arte.', image: 'https://via.placeholder.com/150' },
  { id: 9, name: 'María', age: 29, equipo: 'Betis', description: 'Apasionada por la escritura y los idiomas.', image: 'https://via.placeholder.com/150' },
  { id: 10, name: 'Gonzalo', age: 29, equipo: 'Betis', description: 'Fanático de la historia y los documentales.', image: 'https://via.placeholder.com/150' }
];

const nieto = computed(() => nietos.find(n => n.id === parseInt(route.params.id)));
const currentIndex = computed(() => nietos.findIndex(n => n.id === parseInt(route.params.id)));
const previousNieto = computed(() => (currentIndex.value > 0 ? nietos[currentIndex.value - 1].id : null));
const nextNieto = computed(() => (currentIndex.value < nietos.length - 1 ? nietos[currentIndex.value + 1].id : null));
</script>

<style scoped>
img {
  max-width: 100%;
  height: auto;
}
</style>