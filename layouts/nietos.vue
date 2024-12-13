// layouts/nietoLayout.vue
<template>
  <div>
    <header class="py-6 px-6 flex justify-between items-center bg-gradient-to-r from-gray-200 via-orange-100 to-gray-200">
      <div>
        <h2 class="font-bold text-2xl">
          Detalles del Nieto
        </h2>
      </div>
      <nav>
        <ul class="flex gap-4 font-bold">
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/" exact-active-class="text-blue-500">Inicio</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/about" exact-active-class="text-blue-500">Sobre el abuelo</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/experimento" exact-active-class="text-blue-500">El experimento</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/proyectos" exact-active-class="text-blue-500">Proyectos</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/contacto" exact-active-class="text-blue-500">Contacto</nuxt-link>
          </li>
        </ul>
      </nav>
    </header>

    <main class="p-4">
      <slot />
    </main>
    <footer class="bg-gray-800 text-white py-6 mt-8">
      <div class="text-center">
        <p>&copy; 2024 El sueño de los 95. Todos los derechos reservados.</p>
      </div>
    </footer>
  </div>
</template>

<script setup>
</script>

<style scoped>
</style>