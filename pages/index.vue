// pages/index.vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">¡Bienvenidos a la Celebración del 95º Cumpleaños!</h2>
    <section class="space-y-4">
      <p class="text-gray-700 text-center">
        Este es un espacio dedicado a honrar los 95 años de vida de nuestro querido abuelo. En esta página especial, 
        celebramos su legado, su amor incondicional, y el impacto que ha tenido en nuestras vidas.
      </p>
      <h3 class="text-xl font-bold text-center">Sus Nietos</h3>
      <ul class="list-disc list-inside text-gray-700">
        <li v-for="nieto in nietos" :key="nieto.id">
          <nuxt-link :to="`/nietos/${nieto.id}`" class="text-blue-500 hover:underline">{{ nieto.name }}</nuxt-link>
        </li>
      </ul>
      <h3 class="text-xl font-bold text-center">Sus Dos Mujeres</h3>
      <p class="text-gray-700 text-center">
        Queremos también dedicar un momento especial para destacar a las dos mujeres que han sido pilares fundamentales 
        en su vida, quienes han compartido risas, lágrimas, y un sinfín de momentos memorables junto a él.
      </p>
      <h3 class="text-xl font-bold text-center">Explora Más</h3>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
        <div class="bg-white shadow rounded-lg p-4 text-center">
          <h4 class="font-bold text-lg mb-2">Página de Juego</h4>
          <p class="text-gray-700 mb-2">¡Descubre un divertido juego diseñado para entretener a toda la familia!</p>
          <nuxt-link to="/juego" class="text-blue-500 hover:underline">Ir a la Página de Juego</nuxt-link>
        </div>
        <div class="bg-white shadow rounded-lg p-4 text-center">
          <h4 class="font-bold text-lg mb-2">El Experimento</h4>
          <p class="text-gray-700 mb-2">Conoce más sobre el emocionante experimento de hidrólisis del agua.</p>
          <nuxt-link to="/experimento" class="text-blue-500 hover:underline">Ir al Experimento</nuxt-link>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const nietos = [
  { id: 1, name: 'Nieto 1' },
  { id: 2, name: 'Nieto 2' },
  { id: 3, name: 'Nieto 3' },
  { id: 4, name: 'Nieto 4' },
  { id: 5, name: 'Nieto 5' },
  { id: 6, name: 'Nieto 6' },
  { id: 7, name: 'Nieto 7' },
  { id: 8, name: 'Nieto 8' },
  { id: 9, name: 'Nieto 9' },
  { id: 10, name: 'Nieto 10' },
  { id: 11, name: 'Nieto 11' }
];
</script>

<style scoped>
</style>