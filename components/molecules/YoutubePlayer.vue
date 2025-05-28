<script setup>
const props = defineProps({
  videoId: {
    type: String,
    required: true,
  },
})

const embedUrl = `https://www.youtube.com/embed/${props.videoId}?rel=0`
</script>
<template>
   <div class="p-4 text-center max-w-3xl mx-auto mb-4">
    <div class="lg:text-center mb-6">
        <h2 class="text-base text-blue-600 font-semibold tracking-wide uppercase">Nosso Trabalho</h2>
        <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
          Assista a Resultados Do Nosso Trabalho
        </p>
    </div>
     <div class="w-full aspect-video rounded-2xl overflow-hidden shadow-lg">
    <iframe
      :src="embedUrl"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
      class="w-full h-full"
    ></iframe>
  </div>
  </div>
</template>