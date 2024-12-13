// pages/experimento.vue
<template>
  <div>
    <h2 class="text-2xl font-bold text-center mb-6">El Experimento</h2>
    <section class="space-y-6">
      <!-- Introducción -->
      <p class="text-gray-700 text-justify leading-relaxed">
        La hidrólisis del agua es un proceso que utiliza electricidad para descomponer el agua (H<sub>2</sub>O) en oxígeno (O<sub>2</sub>) e hidrógeno (H<sub>2</sub>).
        Este hidrógeno puede utilizarse como una fuente de energía limpia, esencial en la transición hacia un futuro sostenible. El hidrógeno verde, producido mediante fuentes de energía renovable como la solar o la eólica, es fundamental para reducir la huella de carbono a nivel global.
      </p>

      <!-- Imagen central con animación -->
      <div class="flex justify-center items-center">
        <img src="../assets/images/electrolisis.jpg" alt="Hidrólisis del agua" 
             class="max-w-sm rounded shadow-sm transform transition-transform duration-500 hover:scale-110">
      </div>

      <!-- Importancia del Hidrógeno Verde -->
      <h3 class="text-xl font-bold text-center mt-6">¿Por qué es importante el hidrógeno verde?</h3>
      <ul class="list-disc list-inside space-y-2 text-gray-700">
        <li>Es una fuente de energía renovable y limpia.</li>
        <li>Reduce la dependencia de combustibles fósiles.</li>
        <li>Contribuye a la disminución de emisiones de gases de efecto invernadero.</li>
        <li>Abre nuevas oportunidades para tecnologías de transporte sostenible como vehículos de hidrógeno.</li>
      </ul>

      <!-- Beneficios adicionales con ilustración -->
      <div class="flex flex-col md:flex-row items-center gap-6 mt-6">
        <img src="../assets/images/energia_sostenible.jpg" alt="Energía sostenible"
             class="rounded shadow-md w-full md:w-1/2 transform transition-transform duration-500 hover:scale-105">
        <div class="text-gray-700 text-justify leading-relaxed">
          <h4 class="text-lg font-bold mb-2">Más beneficios</h4>
          <p>
            El hidrógeno verde no solo ofrece una alternativa para generar energía limpia, sino que también puede almacenarse y transportarse de forma eficiente.
            Además, su producción y uso fomentan la independencia energética y la creación de empleos en sectores de energías renovables.
          </p>
        </div>
      </div>

      <!-- Desafíos Actuales con animación -->
      <h3 class="text-xl font-bold text-center mt-8">Desafíos actuales</h3>
      <div class="p-4 bg-yellow-100 rounded shadow-md transition-all duration-500 hover:bg-yellow-200">
        <p class="text-gray-700 leading-relaxed">
          Aunque prometedor, el hidrógeno verde enfrenta desafíos como:
        </p>
        <ul class="list-disc list-inside space-y-2 text-gray-700">
          <li>Alto costo de producción en comparación con alternativas no renovables.</li>
          <li>Infraestructura limitada para su transporte y almacenamiento.</li>
          <li>Eficiencia energética aún por optimizar.</li>
        </ul>
      </div>

      <!-- Conclusión con llamado a la acción -->
      <div class="text-center mt-8">
        <h4 class="text-lg font-bold mb-4">Únete al cambio</h4>
        <p class="text-gray-700 mb-6">
          La transición hacia un futuro sostenible depende de nuestra capacidad para adoptar tecnologías limpias como el hidrógeno verde. Es momento de invertir en el planeta.
        </p>
        <button class="px-6 py-3 bg-blue-500 text-white rounded shadow-lg hover:bg-blue-600 focus:outline-none focus:ring focus:ring-blue-300">
          Aprende más
        </button>
      </div>
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