<script setup>
import { SparklesIcon, ShieldCheckIcon, ChartBarIcon, SunIcon } from '@heroicons/vue/24/outline'

const features = [
  {
    name: 'Limpeza Profissional',
    description: 'Utilizamos produtos e equipamentos especializados para uma limpeza eficiente e segura dos seus painéis.',
    icon: SparklesIcon,
  },
  {
    name: 'Manutenção Preventiva',
    description: 'Identificamos e prevenimos problemas antes que eles afetem o desempenho do seu sistema.',
    icon: ShieldCheckIcon,
  },
  {
    name: 'Monitoramento de Eficiência',
    description: 'Acompanhamos os resultados antes e depois da limpeza para garantir máxima performance.',
    icon: ChartBarIcon,
  },
  {
    name: 'Consultoria Solar',
    description: 'Orientação especializada para maximizar o retorno do seu investimento em energia solar.',
    icon: SunIcon,
  },
]
</script>
<template>
  <div id="services" class="py-12 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="lg:text-center">
        <h2 class="text-base text-blue-600 font-semibold tracking-wide uppercase">Nossos Serviços</h2>
        <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
          Soluções Completas em Limpeza Solar
        </p>
      </div>

      <div class="mt-10">
        <div class="space-y-10 md:space-y-0 md:grid md:grid-cols-2 md:gap-x-8 md:gap-y-10">
          <div v-for="feature in features" :key="feature.name" class="relative">
            <div class="relative">
              <div
                class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-blue-500 text-white">
                <component :is="feature.icon" class="h-6 w-6" aria-hidden="true" />
              </div>
              <p class="ml-16 text-lg leading-6 font-medium text-gray-900">{{ feature.name }}</p>
            </div>
            <div class="mt-2 ml-16 text-base text-gray-500">
              {{ feature.description }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>