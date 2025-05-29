<script setup lang="ts">
import AppHead from '~/components/organisms/AppHead.vue';
import NavBar from '~/components/organisms/NavBar.vue';
import Header from '~/components/organisms/Header.vue';
import Slider from '~/components/organisms/Slider.vue';
import Services from '~/components/organisms/Services.vue';
import AboutCompany from '~/components/organisms/AboutCompany.vue';
import Results from '~/components/organisms/Results.vue';
import ContactForm from '~/components/organisms/ContactForm.vue';
import Footer from '~/components/organisms/Footer.vue';
import YoutubePlayer from '~/components/molecules/YoutubePlayer.vue';
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