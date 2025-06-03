<script setup lang="ts">
import { onMounted } from 'vue';

declare global {
  interface Window {
    dataLayer: any[];
  }
}

function loadScript(src: string): Promise<void> {
  return new Promise((resolve, reject) => {
    if (document.querySelector(`script[src="${src}"]`)) {
      resolve();
      return;
    }
    const script = document.createElement('script');
    script.async = true;
    script.src = src;
    script.onload = () => resolve();
    script.onerror = () => reject(new Error(`Erro ao carregar script: ${src}`));
    document.head.appendChild(script);
  });
}

onMounted(async () => {
  try {
    await loadScript('https://www.googletagmanager.com/gtag/js?id=AW-17134006718');

    window.dataLayer = window.dataLayer || [];
    function gtag(...args: any[]) {
      window.dataLayer.push(args);
    }

    gtag('js', new Date());
    gtag('config', 'AW-17134006718');

    gtag('event', 'conversion', {
      'send_to': 'AW-17134006718/k2ebCI2d3NIaEL7jkOo_'
    });

    console.log('Google Ads Pixel carregado com sucesso.');

  } catch (error) {
    console.error('Erro ao carregar Google Ads Pixel:', error);
  }
});
</script>

<template>
  <!-- Pixel component, sem render -->
</template>
