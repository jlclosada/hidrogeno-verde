// pages/nietos/[id].vue
<template>
  <div>
    <h2 class="text-4xl font-bold text-center mb-6">{{ nieto.name }}</h2>
    <div class="text-center">
      <img :src="nieto.image" :alt="`Imagen de ${nieto.name}`" class="rounded shadow mb-4 mx-auto w-96 h-96 object-cover hover:scale-105 transition ease-linear" />
    </div>
    <div class="flex flex-col bg-slate-200 mx-auto p-4 rounded shadow-md max-w-2xl text-xl">
      <p class="text-gray-900 font-bold py-2">Edad: <span class="text-gray-700 mx-2">{{ nieto.age }}</span></p>
      <p class="text-gray-900 font-bold py-2">Equipo: <span class="text-gray-700 mx-2">{{ nieto.equipo }}</span></p>
      <p class="text-gray-900 font-bold py-2">Descripción: <span class="text-gray-700 mx-2">{{ nieto.description }}</span></p>
      <p class="text-gray-900 font-bold py-2">¿Gradudado?: <span class="text-gray-700 mx-2">{{ nieto.graduado }}</span></p>
    </div>
    <div class="flex justify-center mt-6 my-6">
      <nuxt-link :to="`/nietos/${previousNieto}`" v-if="previousNieto" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600 mx-4">Anterior</nuxt-link>
      <nuxt-link :to="`/nietos/${nextNieto}`" v-if="nextNieto" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">Siguiente</nuxt-link>
    </div>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router';
import { computed } from 'vue';
import fernandoImage from '~/assets/images/fernando.jpeg';
import wisoImage from '~/assets/images/wiso2.jpeg';
import juanImage from '~/assets/images/juan.jpeg';
import manuImage from '~/assets/images/manu.jpeg';
import franImage from '~/assets/images/fran.jpeg';

definePageMeta({
  layout: 'nietos'
});

const route = useRoute();
const nietos = [
  { id: 1, name: 'Fernando', age: 33, equipo: 'Betis', description: 'Fanático de los deportes y la tecnología.', image: fernandoImage, graduado: 'Sí' },
  { id: 2, name: 'José Luis', age: 29, equipo: 'Sevilla', description: 'Le encanta la música clásica y tocar guitarra.', image: wisoImage, graduado: 'Sí' },
  { id: 3, name: 'Kike', age: 29, equipo: 'Betis', description: 'Aficionado a los videojuegos y los cómics.', image: 'https://via.placeholder.com/150', graduado: 'No' },
  { id: 4, name: 'Pablo', age: 27, equipo: 'Barcelona', description: 'Entusiasta de la cocina y los viajes.', image: 'https://via.placeholder.com/150', graduado: 'No' },
  { id: 5, name: 'Manuel', age: 29, equipo: 'Vodka', description: 'Amante de las fiestas y el baile.', image: manuImage, graduado: 'No' },
  { id: 6, name: 'Javier', age: 29, equipo: 'Sevilla', description: 'Disfruta de la lectura y el senderismo.', image: 'https://via.placeholder.com/150', graduado: 'No' },
  { id: 7, name: 'Juan', age: 29, equipo: 'Betis', description: 'Disfruta de la lectura y el senderismo.', image: juanImage, graduado: 'No' },
  { id: 8, name: 'Manolo', age: 29, equipo: 'Sevilla', description: 'Apasionado por el cine y la fotografía.', image: 'https://via.placeholder.com/150', graduado: 'No' },
  { id: 9, name: 'Fran', age: 29, equipo: 'Betis', description: 'Le encanta el diseño gráfico y el arte.', image: franImage, graduado: 'No' },
  { id: 10, name: 'María', age: 29, equipo: 'Betis', description: 'Apasionada por la escritura y los idiomas.', image: 'https://via.placeholder.com/150', graduado: 'No' },
  { id: 11, name: 'Gonzalo', age: 29, equipo: 'Betis', description: 'Fanático de la historia y los documentales.', image: 'https://via.placeholder.com/150', graduado: 'No' }
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