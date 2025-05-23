<script setup>
const navigation = [
  { name: 'Início', href: '#' },
  { name: 'Serviços', href: '#services' },
  { name: 'Sobre', href: '#about' },
  { name: 'Resultados', href: '#results' },
  { name: 'Contato', href: '#contact' },
]
</script>

<template>
  <nav class="bg-blue-600 fixed w-full z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex-shrink-0">
          <img class="h-28 mt-2 w-auto" src="/public/logo.png" alt="Logo" />
        </div>
        <div class="hidden md:block">
          <div class="ml-10 flex items-baseline space-x-4">
            <NuxtLink v-for="item in navigation" :key="item.name" :to="item.href"
              class="text-white hover:bg-blue-700 px-3 py-2 rounded-md text-sm font-medium">
              {{ item.name }}
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>