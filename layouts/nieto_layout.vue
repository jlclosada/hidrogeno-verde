// layouts/nietoLayout.vue
<template>
  <div>
    <header class="bg-gray-800 text-white p-4 text-center">
      <h1 class="text-2xl font-bold">Detalles del Nieto</h1>
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