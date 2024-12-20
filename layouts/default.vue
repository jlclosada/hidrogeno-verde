<template>
  <div>
    <header class="py-6 px-6 flex justify-between items-center bg-gradient-to-r from-orange-200 via-orange-100 to-orange-200">
      <div>
        <h2 class="font-bold text-xl transform hover:scale-105 transition duration-300 ease-in-out">
          <nuxt-link to="/">El sueño de Manuel Losada Villasante</nuxt-link>
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
          <li class="text-blue-800 hover:text-blue-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/#hijos" exact-active-class="text-blue-500">Hijos</nuxt-link>
          </li>
          <li class="text-green-800 hover:text-green-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/#nietos" exact-active-class="text-blue-500">Nietos</nuxt-link>
          </li>
          <li class="text-pink-800 hover:text-pink-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/#damas" exact-active-class="text-blue-500">Damas</nuxt-link>
          </li>
          <li class="text-gray-800 hover:text-gray-500 transform hover:scale-110 transition duration-300 ease-in-out py-2 rounded">
            <nuxt-link to="/contacto" exact-active-class="text-blue-500">Contacto</nuxt-link>
          </li>
        </ul>
      </nav>
    </header>

    <div mt-8>
      <slot />
    </div>

    <footer class="bg-slate-950 text-white py-6">
      <div class="text-center">
        <p class="footer-rights mb-4">&copy; 2024 El sueño de los 95. Todos los derechos reservados.</p>
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
  color: #07295f;
  font-weight: bold;
}
</style>
