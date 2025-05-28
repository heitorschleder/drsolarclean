<script setup>
import { BoltIcon, SunIcon, ArrowTrendingUpIcon } from '@heroicons/vue/24/outline'

const testimonials = [
  {
    title: 'Aumento de Produção',
    content: 'Após a limpeza, nossa produção de energia aumentou em visívelmente. O investimento se pagou em menos de 3 meses!',
    author: 'João Silva - Residencial',
    icon: BoltIcon,
  },
  {
    title: 'Manutenção Preventiva',
    content: 'A limpeza regular nos ajudou a identificar e prevenir problemas antes que afetassem nosso sistema.',
    author: 'Maria Santos - Comercial',
    icon: SunIcon,
  },
  {
    title: 'Retorno do Investimento',
    content: 'Com o aumento da eficiência, conseguimos um retorno mais rápido do nosso investimento em energia solar.',
    author: 'Pedro Costa - Industrial',
    icon: ArrowTrendingUpIcon,
  },
]
</script>

<template>
  <div id="results" class="bg-white py-16 sm:py-24">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center">
        <h2 class="text-base font-semibold text-blue-600 tracking-wide uppercase">Resultados</h2>
        <p class="mt-1 text-4xl font-extrabold text-gray-900 sm:text-5xl sm:tracking-tight lg:text-6xl">
          Números que Comprovam
        </p>
        <p class="max-w-xl mt-5 mx-auto text-xl text-gray-500">
          Confira os resultados reais obtidos por nossos clientes após nossa limpeza profissional
        </p>
      </div>

      <div class="mt-12">
        <div class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3">
          <div v-for="testimonial in testimonials" :key="testimonial.author"
            class="pt-6">
            <div class="flow-root bg-gray-50 rounded-lg px-6 pb-8">
              <div class="-mt-6">
                <div class="inline-flex items-center justify-center p-3 bg-blue-500 rounded-md shadow-lg">
                  <component :is="testimonial.icon" class="h-6 w-6 text-white" aria-hidden="true" />
                </div>
                <h3 class="mt-8 text-lg font-medium text-gray-900 tracking-tight">{{ testimonial.title }}</h3>
                <p class="mt-5 text-base text-gray-500">{{ testimonial.content }}</p>
                <p class="mt-5 text-sm font-medium text-gray-900">{{ testimonial.author }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>