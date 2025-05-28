<script setup>
const navigation = [
  { name: 'Sobre', href: '#about' },
  { name: 'Serviços', href: '#services' },
  { name: 'Resultados', href: '#results' },
  { name: 'Contato', href: '#contact' },
]

const social = [

]
</script>
<template>
  <footer class="bg-blue-600">
    <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
      <nav class="-mx-5 -my-2 flex flex-wrap justify-center">
        <div v-for="item in navigation" :key="item.name" class="px-5 py-2">
          <a :href="item.href" class="text-base text-white hover:text-blue-200">
            {{ item.name }}
          </a>
        </div>
      </nav>
      <div class="mt-8 flex justify-center space-x-6">
        <a v-for="item in social" :key="item.name" :href="item.href" class="text-white hover:text-blue-200">
          <span class="sr-only">{{ item.name }}</span>
          <component :is="item.icon" class="h-6 w-6" aria-hidden="true" />
        </a>
      </div>
      <p class="mt-8 text-center text-base text-white">
        &copy; 2024 Dr. Solar Clean. Todos os direitos reservados.
      </p>
    </div>
  </footer>
</template>