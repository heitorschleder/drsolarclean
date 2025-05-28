<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'

import limpeza1 from '~/public/images/image-1.jpg'
import limpeza2 from '~/public/images/image-2.jpg'
import limpeza3 from '~/public/images/image-3.jpg'
import limpeza4 from '~/public/images/image-4.jpg'
import limpeza5 from '~/public/images/image-5.jpg'
import limpeza6 from '~/public/images/image-6.jpg'
import limpeza7 from '~/public/images/image-7.jpg'
import limpeza8 from '~/public/images/image-8.jpg'
import limpeza9 from '~/public/images/image-9.jpg'

const images = [
  limpeza1,
  limpeza2,
  limpeza3,
  limpeza4,
  limpeza5,
  limpeza6,
  limpeza7,
  limpeza8,
  limpeza9,
]

const showModal = ref(false)
const selectedImage = ref(null)

const openModal = (img) => {
  selectedImage.value = img
  showModal.value = true
}

const closeModal = () => {
  showModal.value = false
}
</script>

<template>
  <section class="py-8 px-4 bg-white">
    <div class="lg:text-center mb-8">
      <h2 class="text-base text-blue-600 font-semibold tracking-wide uppercase">Nosso Trabalho</h2>
      <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">
        Veja Resultados Reais
      </p>
    </div>

    <Swiper
      :loop="true"
      :autoplay="{ delay: 3000 }"
      class="max-w-md mx-auto rounded-lg shadow-md"
    >
      <SwiperSlide v-for="(img, i) in images" :key="i">
        <img
          :src="img"
          alt=""
          class="w-full h-72 object-cover cursor-pointer"
          @click="openModal(img)"
        />
      </SwiperSlide>
    </Swiper>

    <!-- Modal -->
    <div
      v-if="showModal"
      class="fixed inset-0 bg-black bg-opacity-80 flex items-center justify-center z-50"
      @click.self="closeModal"
    >
      <div class="relative max-w-3xl w-full p-4">
        <button
          @click="closeModal"
          class="absolute top-4 right-4 text-white text-2xl font-bold hover:text-gray-300"
        >
          ×
        </button>
        <img :src="selectedImage" alt="Imagem expandida" class="w-full max-h-[90vh] object-contain rounded-lg" />
      </div>
    </div>
  </section>
</template>