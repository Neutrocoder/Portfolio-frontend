<script setup>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import About from "./components/About.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
    <Header />
        <main id="home">
            <Hero />
            <About />
            <Projects />
            <Contact />
        </main>
    <Footer />
</template>

<style scoped>

</style>
