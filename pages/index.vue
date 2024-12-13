<template>
  <div class="bg-gradient-to-r from-orange-50 via-orange-100 to-orange-50 border-b-2 border-gray-500">
    <h2 class="text-4xl font-bold text-center text-gray-800 text-shadow-lg py-6">
      ¡Bienvenidos a la Celebración del 95º Cumpleaños!
    </h2>

    <!-- Descripción -->
    <p class="text-xl text-center mx-auto max-w-3xl mt-6 text-gray-700 font-light">
      Este es un espacio dedicado a honrar los 95 años de vida de nuestro querido <b>abuelo</b> y también a nuestra <b>abuela</b>. En esta página especial, 
      celebramos su legado, su amor incondicional, y el impacto que ha tenido en nuestras vidas.
    </p>
    <div class="text-center mt-6 flex items-center justify-center">
      <!-- <img src="../assets/images/abuelos_boda.jpeg" alt="Abuelos de boda" class="rounded shadow mb-4 mx-auto object-cover w-auto h-64 hover:scale-110 transition ease-linear" /> -->
      <!-- <img src="../assets/images/abuelo_joven.jpeg" alt="Abuelos de boda" class="rounded shadow mb-4 mx-auto object-cover w-auto h-64 hover:scale-110 transition ease-linear" /> -->
      <img src="../assets/images/familia.jpeg" alt="Abuelos de boda" class="rounded shadow mb-4 mx-auto object-cover w-auto hover:scale-105 transition ease-linear" />
      <!-- <img src="../assets/images/abuelo_nieves.jpeg" alt="Abuelos de boda" class="rounded shadow mb-4 mx-auto object-cover w-64 h-64 hover:scale-110 transition ease-linear" /> -->
      <!-- <img src="../assets/images/abuelo_plantas.jpeg" alt="Abuelos de boda" class="rounded shadow mb-4 mx-auto object-cover w-64 h-64 hover:scale-110 transition ease-linear" /> -->
    </div>

    <!-- Secciones de Hijos, Nietos y Primeras Damas -->
    <section class="mt-12 space-y-8 px-4">
      
      <!-- Sección de Hijos -->
      <div class="section-container w-auto">
        <h3 class="text-3xl font-semibold text-center text-gray-800 mb-4">Los Hijos/as</h3>
        <p class="text-xl text-center mx-auto max-w-3xl mt-6 text-gray-700 font-light">
          Este es un espacio dedicado a honrar los 95 años de vida de nuestro querido abuelo. En esta página especial, 
          celebramos su legado, su amor incondicional, y el impacto que ha tenido en nuestras vidas.
        </p>
        <img src="../assets/images/hijos_sofa.jpeg" alt="Abuelos de boda" class="rounded shadow mb-4 mt-4 mx-auto object-fill h-64 w-96 hover:scale-105 transition ease-linear" />
        <ul class="flex flex-wrap justify-center gap-6 py-4">
          <li v-for="hijo in hijos" :key="hijo.id" class="hover:scale-105 transform transition duration-300">
            <nuxt-link 
              :to="`/hijos/${hijo.id}`" 
              class="text-2xl text-gray-600 hover:text-orange-800 hover:underline font-semibold mx-2">
              {{ hijo.name }}
            </nuxt-link>
          </li>
        </ul>
      </div>

      <!-- Sección de Nietos -->
      <div class="section-container">
        <h3 class="text-3xl font-semibold text-center text-gray-800 mb-4">Los Nietos</h3>
        <p class="text-xl text-center mx-auto max-w-3xl mt-6 text-gray-700 font-light">
          Este es un espacio dedicado a honrar los 95 años de vida de nuestro querido abuelo. En esta página especial, 
          celebramos su legado, su amor incondicional, y el impacto que ha tenido en nuestras vidas.
        </p>
        <div class="container mx-auto flex flex-wrap justify-center gap-6">
          <img src="../assets/images/primos2.jpeg" alt="Abuelos de boda" class="rounded shadow mb-4 mt-4 mx-auto object-fill w-96 h-auto hover:scale-105 transition ease-linear" />
        </div>
        <ul class="flex flex-wrap justify-center gap-6 py-4">
          <li v-for="nieto in nietos" :key="nieto.id" class="hover:scale-105 transform transition duration-300">
            <nuxt-link 
              :to="`/nietos/${nieto.id}`" 
              class="text-2xl text-green-800 hover:text-orange-800 hover:underline font-semibold">
              {{ nieto.name }}
            </nuxt-link>
          </li>
        </ul>
      </div>

      <!-- Sección de Primeras Damas -->
      <div class="section-container">
        <h3 class="text-3xl font-semibold text-center text-gray-800 mb-4">Las Primeras Damas</h3>
        <p class="text-xl text-center mx-auto max-w-3xl mt-6 text-gray-700 font-light">
          Este es un espacio dedicado a honrar los 95 años de vida de nuestro querido abuelo. En esta página especial, 
          celebramos su legado, su amor incondicional, y el impacto que ha tenido en nuestras vidas.
        </p>
        <ul class="flex flex-wrap justify-center gap-6 py-4">
          <li v-for="dama in primerasDamas" :key="dama.id" class="hover:scale-105 transform transition duration-300">
            <nuxt-link 
              :to="`/damas/${dama.id}`" 
              class="text-2xl text-purple-600 hover:text-purple-800 hover:underline font-semibold">
              {{ dama.name }}
            </nuxt-link>
          </li>
        </ul>
      </div>

      <!-- Explora Más -->
      <h3 class="text-2xl font-semibold text-center text-gray-800 mt-12">Explora Más</h3>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 px-4 mt-6 mb-12">
        <div class="bg-white rounded-lg shadow-lg p-6 hover:scale-105 transform transition duration-300 border-2 border-gray-200">
          <h4 class="font-semibold text-xl mb-2 text-gray-800">Página de Juego</h4>
          <p class="text-gray-700 mb-2">¡Descubre un divertido juego diseñado para entretener a toda la familia!</p>
          <nuxt-link to="/juego" class="text-indigo-500 hover:text-indigo-700">Ir a la Página de Juego</nuxt-link>
        </div>
        <div class="bg-white rounded-lg shadow-lg p-6 hover:scale-105 transform transition duration-300 border-2 border-gray-200">
          <h4 class="font-semibold text-xl mb-2 text-gray-800">El Experimento</h4>
          <p class="text-gray-700 mb-2">Conoce más sobre el emocionante experimento de hidrólisis del agua.</p>
          <nuxt-link to="/experimento" class="text-indigo-500 hover:text-indigo-700">Ir al Experimento</nuxt-link>
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
    { id: 2, name: 'Alejandra' }
]

const hijos = [
    { id: 1, name: 'Patricia' },
    { id: 2, name: 'María' },
    { id: 3, name: 'Nieves' },
    { id: 4, name: 'Manolo' }
]
</script>

<style scoped>
/* Fondo de las secciones */
.section-container {
  border-radius: 10px;
  padding: 20px;
  margin-bottom: 20px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

html, body {
  height: 100%;
  margin:0;
  padding: 0;
  font-family: 'Poppins', sans-serif;
  background-color: antiquewhite;
}

/* Fondo para el cuerpo de la página */
body {
  background: linear-gradient(to right, #e6eaeb, #682574); /* Puedes ajustar este gradiente */
}

/* Efectos para enlaces */
.nuxt-link:hover {
  transform: translateY(-2px);
  transition: transform 0.3s ease;
}

/* Estilos para las listas */
ul {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  justify-content: center;
}

li {
  font-size: 1.2rem;
  font-weight: 600;
}

.text-shadow-lg {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
}
</style>
