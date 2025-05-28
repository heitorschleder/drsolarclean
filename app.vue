<script setup lang="ts">
useHead({
  title: 'Dr. Solar Clean',
  meta: [
    { name: 'description', content: 'Veja os resultados reais dos nossos serviços de limpeza e transformação.' },
    { property: 'og:title', content: 'Dr. Solar Clean' },
    { property: 'og:description', content: 'Veja os resultados reais dos nossos serviços de limpeza e transformação.' },
    {
      property: 'og:image',
      content: 'https://i.imgur.com/UvAWsrr.png'
    },
    { property: 'og:type', content: 'website' },
    { property: 'og:url', content: 'https://drsolarclean.com.br' },
    { name: 'twitter:card', content: 'summary_large_image' }
  ]
})
</script>
<template>
  <div>
    <NuxtPage />
  </div>
</template>