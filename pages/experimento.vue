// pages/experimento.vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">El Experimento</h2>
    <section class="space-y-4">
      <p class="text-gray-700">
        La hidrólisis del agua es un proceso que utiliza electricidad para descomponer el agua (H<sub>2</sub>O) en oxígeno (O<sub>2</sub>) e hidrógeno (H<sub>2</sub>).
        Este hidrógeno puede utilizarse como una fuente de energía limpia, esencial en la transición hacia un futuro sostenible.
      </p>
      <img src="https://ptx-hub.org/wp-content/uploads/2021/05/Own-depiction-of-PEM-electrolysis-based-on-1-1024x831.png" alt="Hidrólisis del agua" class="mx-auto rounded shadow-sm h-250">
      <h3 class="text-xl font-bold">¿Por qué es importante el hidrógeno verde?</h3>
      <ul class="list-disc list-inside space-y-2">
        <li>Es una fuente de energía renovable y limpia.</li>
        <li>Reduce la dependencia de combustibles fósiles.</li>
        <li>Contribuye a la disminución de emisiones de gases de efecto invernadero.</li>
      </ul>
      <h3 class="text-xl font-bold">Desafíos actuales</h3>
      <p class="text-gray-700">
        Aunque prometedor, el hidrógeno verde enfrenta desafíos como el alto costo de producción, la infraestructura limitada y la eficiencia energética.
      </p>
    </section>
  </div>
</template>

<script setup>
</script>

<style scoped>
img {
  max-width: 100%;
  height: auto;
}
</style>