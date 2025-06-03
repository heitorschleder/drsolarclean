<script setup lang="ts">
import { onMounted } from 'vue';

onMounted(() => {
  const script1 = document.createElement('script');
  script1.async = true;
  script1.src = 'https://www.googletagmanager.com/gtag/js?id=AW-17134006718';
  document.head.appendChild(script1);

  const script2 = document.createElement('script');
  script2.text = `
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'AW-17134006718');
    gtag('event', 'conversion', {'send_to': 'AW-17134006718/k2ebCI2d3NIaEL7jkOo_'});
  `;
  document.head.appendChild(script2);
});
</script>

<template>
    <main>
        <AppHead />
        <NavBar />
        <Header />
        <Slider />
        <Services />
        <YoutubePlayer video-id="Rv4hVnjk7m4" />
        <AboutCompany />
        <Results /> 
        <YoutubePlayer video-id="UxkupSgfavM" />
        <ContactForm />
        <Footer />
    </main>
</template>
