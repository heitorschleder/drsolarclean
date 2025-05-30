<script setup>
import { ref } from 'vue'

const navigation = [
  { name: 'Início', href: '#' },
  { name: 'Serviços', href: '#services' },
  { name: 'Sobre', href: '#about' },
  { name: 'Resultados', href: '#results' },
  { name: 'Contato', href: '#contact' },
]

const isOpen = ref(false)
</script>

<template>
  <nav class="bg-blue-600 fixed w-full z-50 h-20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-full flex items-center justify-between">
      
      <div class="flex items-center h-full">
        <img src="/public/logo.png" alt="Logo" class="h-28 w-auto object-contain" />
      </div>

      <div class="md:hidden">
        <button @click="isOpen = !isOpen" type="button" class="text-white focus:outline-none">
          <svg class="h-7 w-7" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path v-if="!isOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16" />
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>

      <div class="hidden md:flex space-x-6">
        <NuxtLink
          v-for="item in navigation"
          :key="item.name"
          :to="item.href"
          class="text-white hover:bg-blue-700 px-4 py-2 rounded-md text-sm font-medium"
        >
          {{ item.name }}
        </NuxtLink>
      </div>
    </div>

    <div v-if="isOpen" class="md:hidden px-4 pb-4">
      <div class="flex flex-col space-y-2">
        <NuxtLink
          v-for="item in navigation"
          :key="item.name"
          :to="item.href"
          class="block text-white bg-blue-700 px-3 py-2 rounded-md text-base font-medium"
          @click="isOpen = false"
        >
          {{ item.name }}
        </NuxtLink>
      </div>
    </div>
  </nav>
</template>
