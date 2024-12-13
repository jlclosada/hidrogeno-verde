// pages/hijos/[id].vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">Detalles de {{ hijo.name }}</h2>
    <div class="text-center">
      <img :src="hijo.image" :alt="`Imagen de ${hijo.name}`" class="rounded shadow mb-4 mx-auto w-48 h-48 object-cover" />
    </div>
    <p class="text-gray-700">Edad: {{ hijo.age }}</p>
    <p class="text-gray-700">Equipo: {{ hijo.equipo }}</p>
    <p class="text-gray-700">Descripción: {{ hijo.description }}</p>
    <div class="flex justify-between mt-6">
      <nuxt-link :to="`/hijos/${previousHijo}`" v-if="previousHijo" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">Anterior</nuxt-link>
      <nuxt-link :to="`/hijos/${nextHijo}`" v-if="nextHijo" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">Siguiente</nuxt-link>
    </div>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router';
import { computed } from 'vue';

const route = useRoute();
const hijos = [
  { id: 1, name: 'Patricia', age: 33, equipo: 'Betis', description: 'Fanático de los deportes y la tecnología.', image: 'https://via.placeholder.com/150' },
  { id: 2, name: 'María', age: 29, equipo: 'Sevilla', description: 'Le encanta la música clásica y tocar guitarra.', image: 'https://via.placeholder.com/150' },
  { id: 3, name: 'Nieves', age: 29, equipo: 'Betis', description: 'Aficionado a los videojuegos y los cómics.', image: 'https://via.placeholder.com/150' },
  { id: 4, name: 'Manolo', age: 27, equipo: 'Barcelona', description: 'Entusiasta de la cocina y los viajes.', image: 'https://via.placeholder.com/150' }
];

const hijo = computed(() => hijos.find(n => n.id === parseInt(route.params.id)));
const currentIndex = computed(() => hijos.findIndex(n => n.id === parseInt(route.params.id)));
const previousHijo = computed(() => (currentIndex.value > 0 ? hijos[currentIndex.value - 1].id : null));
const nextHijo = computed(() => (currentIndex.value < hijos.length - 1 ? hijos[currentIndex.value + 1].id : null));
</script>

<style scoped>
img {
  max-width: 100%;
  height: auto;
}
</style>