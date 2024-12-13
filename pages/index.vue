// pages/index.vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6 mx-auto py-8">¡Bienvenidos a la Celebración del 95º Cumpleaños!</h2>
    <section class="space-y-4">
      <p class="text-gray-700 text-center mx-6 text-lg">
        Este es un espacio dedicado a honrar los 95 años de vida de nuestro querido abuelo. En esta página especial, 
        celebramos su legado, su amor incondicional, y el impacto que ha tenido en nuestras vidas.
      </p>
      <h3 class="text-2xl font-bold text-center">Los Hijos/as</h3>
      <ul class="lista-primos list-disc list-inside text-gray-700 flex">
        <li v-for="hijo in hijos" :key="hijo.id">
          <nuxt-link :to="`/hijos/${hijo.id}`" class="text-blue-500 text-xl hover:underline">{{ hijo.name }}</nuxt-link>
        </li>
      </ul>
      <h3 class="text-2xl font-bold text-center">Los Nietos</h3>
      <ul class="lista-primos list-disc list-inside text-gray-700 flex">
        <li v-for="nieto in nietos" :key="nieto.id">
          <nuxt-link :to="`/nietos/${nieto.id}`" class="text-blue-500 text-xl hover:underline">{{ nieto.name }}</nuxt-link>
        </li>
      </ul>
      <h3 class="text-2xl font-bold text-center">Las Primeras Damas</h3>
      <p class="text-gray-700 text-left font-light mx-6">
        Queremos también dedicar un momento especial para destacar a las dos mujeres que han sido pilares fundamentales 
        en su vida, quienes han compartido risas, lágrimas, y un sinfín de momentos memorables junto a él.
      </p>
      <ul class="lista-primos list-disc list-inside text-gray-700 flex">
        <li v-for="dama in primerasDamas" :key="dama.id">
        <NuxtLink :to="`/damas/${dama.id}`" class="text-blue-500 text-xl hover:underline">{{ dama.name }}</NuxtLink></li>
      </ul>
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
  { id: 1, name: 'Fernando' },
  { id: 2, name: 'José Luis' },
  { id: 3, name: 'Kike' },
  { id: 4, name: 'Pablo' },
  { id: 5, name: 'Manuel' },
  { id: 6, name: 'Javier' },
  { id: 7, name: 'Juan' },
  { id: 8, name: 'Manolo' },
  { id: 9, name: 'Fran' },
  { id: 10, name: 'María' },
  { id: 11, name: 'Gonzalo' }
];

const primerasDamas = [
    { id: 1, name: 'Valle' },
    { id: 2, name: 'Alejandra'}
]

const hijos = [
    { id: 1, name: 'Patricia'},
    { id: 2, name: 'María'},
    { id: 3, name: 'Nieves'},
    { id: 4, name: 'Manolo'}
]
</script>

<style scoped>

.lista-primos {
  justify-content: center;
  gap: 1rem;
  margin-top: 1rem;
  list-style: none;
}
</style>