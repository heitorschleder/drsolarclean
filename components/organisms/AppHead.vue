<script setup>
import { useHead } from '#imports'

const props = defineProps({
  title: {
    type: String,
    default: 'Dr. Solar Clean'
  },
  description: {
    type: String,
    default: ''
  },
  image: {
    type: String,
    default: '/thumbnail.jpg'
  },
  url: {
    type:String,
    default: 'https://drsolarclean.com.br'
  }
})

useHead({
  title: props.title,
  meta: [
    { name: 'description', content: props.description },
    { property: 'og:title', content: props.title },
    { property: 'og:description', content: props.description },
    { property: 'og:image', content: props.image },
    { property: 'og:url', content: props.url },
    { name: 'twitter:card', content: 'summary_large_image' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' },
  ],
})
</script>
