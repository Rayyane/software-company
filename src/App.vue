<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue';
import About from './components/About.vue';
import Stats from './components/Stats.vue';
import Services from './components/Services.vue';
import Clients from './components/Clients.vue';
import Testimonials from './components/Testimonials.vue';
import HowWeWork from './components/HowWeWork.vue';
import Faq from './components/Faq.vue';
import CallToAction from './components/CallToAction.vue';
import Team from './components/Team.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';

</script>

<template>
  <Navbar />

  <main class="main">
    <Hero />
    <About />
    <Stats />
    <Services />
    <Clients  />
    <Testimonials />
    <HowWeWork />
    <Faq />
    <CallToAction />
    <Team />
    <Contact />
  </main>
  <Footer />
</template>

<style scoped>

</style>
