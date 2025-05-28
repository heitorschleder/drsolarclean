<script setup>
import { PhoneIcon } from '@heroicons/vue/24/outline'

const whatsappLink = 'https://wa.me/5548984063437?text=Olá!%20Gostaria%20de%20um%20orçamento%20para%20limpeza%20de%20placas%20solares.'
</script>
<template>
  <section id="contact" class="bg-blue-50 py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-xl mx-auto text-center">
      <div class="flex justify-center mb-6">
        <svg class="w-16 h-16 text-blue-600" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round"
            d="M4.5 12h15M12 4.5v15M6.75 6.75l10.5 10.5M17.25 6.75l-10.5 10.5" />
        </svg>
      </div>
      <h2 class="text-2xl sm:text-3xl font-extrabold text-gray-900">
        Solicite seu Orçamento Rápido
      </h2>
      <p class="mt-4 text-lg text-gray-600">
        Fale com a nossa equipe no WhatsApp e receba um orçamento rápido e sem burocracia.
      </p>
      <div class="mt-8">
        <a :href="whatsappLink" target="_blank" rel="noopener"
          class="inline-flex items-center justify-center px-6 py-3 text-white bg-green-600 hover:bg-green-700 rounded-md shadow-lg transition duration-300 text-lg">
          <PhoneIcon class="w-5 h-5 mr-2 text-white" />
          Falar no WhatsApp
        </a>
      </div>
    </div>
  </section>
</template>