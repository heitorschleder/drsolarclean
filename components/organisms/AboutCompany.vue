<script setup>
const stats = [
  { value: '500+', label: 'Clientes Atendidos' },
  { value: '98%', label: 'Satisfação' },
  { value: '30%', label: 'Aumento Médio de Eficiência' },
  { value: '5000+', label: 'Painéis Limpos' },
]
</script>
<template>
  <div id="about" class="bg-blue-50 py-16 lg:py-24">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="lg:grid lg:grid-cols-2 lg:gap-8 lg:items-center">
        <div>
          <h2 class="text-3xl font-extrabold text-gray-900 sm:text-4xl">
            Sobre a Dr. Solar Clean
          </h2>
          <p class="mt-3 max-w-3xl text-lg text-gray-500">
            Desde 2020, somos referência em limpeza e manutenção de painéis solares. Nossa missão é garantir que seu
            investimento em energia solar alcance seu máximo potencial.
          </p>
          <div class="mt-8 sm:flex">
            <div class="rounded-md shadow">
              <a href="#contact"
                class="flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700">
                Fale Conosco
              </a>
            </div>
          </div>
        </div>
        <div class="mt-8 grid grid-cols-2 gap-0.5 md:grid-cols-3 lg:mt-0 lg:grid-cols-2">
          <div v-for="stat in stats" :key="stat.label"
            class="col-span-1 flex justify-center py-8 px-8 bg-white">
            <div class="text-center">
              <span class="text-3xl font-extrabold text-blue-600">
                {{ stat.value }}
              </span>
              <span class="block text-sm font-medium text-gray-500">{{ stat.label }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>