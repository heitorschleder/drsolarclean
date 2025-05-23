<script setup>
import { ref } from 'vue'
import { PhoneIcon, EnvelopeIcon } from '@heroicons/vue/24/outline'

const form = ref({
  name: '',
  email: '',
  message: ''
})

const handleSubmit = () => {
  console.log('Form submitted:', form.value)
}
</script>
<template>
  <div id="contact" class="bg-blue-50 py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-lg mx-auto md:max-w-none md:grid md:grid-cols-2 md:gap-8">
      <div>
        <h2 class="text-2xl font-extrabold text-gray-900 sm:text-3xl">
          Informações de Contato
        </h2>
        <div class="mt-3">
          <p class="text-lg text-gray-500">
            Entre em contato conosco para um orçamento gratuito ou tire suas dúvidas sobre nossos serviços.
          </p>
        </div>
        <div class="mt-9">
          <div class="flex">
            <div class="flex-shrink-0">
              <PhoneIcon class="h-6 w-6 text-blue-600" aria-hidden="true" />
            </div>
            <div class="ml-3 text-base text-gray-500">
              <p>(11) 99999-9999</p>
            </div>
          </div>
          <div class="mt-6 flex">
            <div class="flex-shrink-0">
              <EnvelopeIcon class="h-6 w-6 text-blue-600" aria-hidden="true" />
            </div>
            <div class="ml-3 text-base text-gray-500">
              <p>contato@drsolarclean.com.br</p>
            </div>
          </div>
        </div>
      </div>
      <div class="mt-12 sm:mt-16 md:mt-0">
        <h2 class="text-2xl font-extrabold text-gray-900 sm:text-3xl">
          Solicite um Orçamento
        </h2>
        <div class="mt-9">
          <form @submit.prevent="handleSubmit" class="grid grid-cols-1 gap-y-6">
            <div>
              <label for="name" class="block text-sm font-medium text-gray-700">Nome</label>
              <div class="mt-1">
                <input type="text" name="name" id="name" v-model="form.name"
                  class="py-3 px-4 block w-full shadow-sm focus:ring-blue-500 focus:border-blue-500 border-gray-300 rounded-md" />
              </div>
            </div>
            <div>
              <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
              <div class="mt-1">
                <input type="email" name="email" id="email" v-model="form.email"
                  class="py-3 px-4 block w-full shadow-sm focus:ring-blue-500 focus:border-blue-500 border-gray-300 rounded-md" />
              </div>
            </div>
            <div>
              <label for="message" class="block text-sm font-medium text-gray-700">Mensagem</label>
              <div class="mt-1">
                <textarea id="message" name="message" rows="4" v-model="form.message"
                  class="py-3 px-4 block w-full shadow-sm focus:ring-blue-500 focus:border-blue-500 border-gray-300 rounded-md"></textarea>
              </div>
            </div>
            <div>
              <button type="submit"
                class="w-full inline-flex justify-center py-3 px-6 border border-transparent shadow-sm text-base font-medium rounded-md text-white bg-blue-600 hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500">
                Enviar
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>