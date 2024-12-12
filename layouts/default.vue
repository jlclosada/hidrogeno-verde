// layout/default.vue
<template>
  <div>
    <header class="mx-auto py-6 px-4 flex justify-between bg-white shadow items-center">
      <div>
        <h2 class="font-bold text-xl transform hover:scale-110 transition duration-300 ease-in-out">
          <nuxt-link to="/">El sueño de los 95</nuxt-link>
        </h2>
      </div>
      <nav>
        <ul class="flex gap-4">
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/">Inicio</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/about">Sobre el abuelo</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/experimento">El experimento</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/proyectos">Proyectos</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/contacto">Contacto</nuxt-link>
          </li>
        </ul>
      </nav>
    </header>

    <div class="mx-auto p-4">
      <slot />
    </div>

    <footer class="bg-gray-800 text-white py-6 mt-8">
      <div class="text-center">
        <p class="mb-4">&copy; 2024 El sueño de los 95. Todos los derechos reservados.</p>
        <div class="flex justify-center gap-6">
          <a href="#" class="hover:text-blue-500">Facebook</a>
          <a href="#" class="hover:text-blue-500">Twitter</a>
          <a href="#" class="hover:text-blue-500">Instagram</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
</script>

<style scoped>
.router-link-exact-active {
  color: #3b82f6;
  font-weight: bold;
}
</style>
