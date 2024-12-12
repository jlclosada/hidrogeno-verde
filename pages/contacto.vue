// pages/contacto.vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">Contacto</h2>
    <form class="max-w-xl mx-auto bg-white shadow rounded-lg p-6 space-y-4">
      <div>
        <label for="name" class="block font-bold">Nombre</label>
        <input
          id="name"
          type="text"
          class="w-full border border-gray-300 rounded p-2"
          placeholder="Ingresa tu nombre"
        />
      </div>
      <div>
        <label for="email" class="block font-bold">Correo</label>
        <input
          id="email"
          type="email"
          class="w-full border border-gray-300 rounded p-2"
          placeholder="Ingresa tu correo"
        />
      </div>
      <div>
        <label for="message" class="block font-bold">Mensaje</label>
        <textarea
          id="message"
          rows="5"
          class="w-full border border-gray-300 rounded p-2"
          placeholder="Escribe tu mensaje aquí"
        ></textarea>
      </div>
      <div class="text-center">
        <button class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">
          Enviar
        </button>
      </div>
    </form>
  </div>
</template>

<script setup>
</script>

<style scoped>
</style>
