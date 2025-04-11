<script setup>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Projects from "./components/Projects.vue";
import About from "./components/About.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
    <Header/>
        <main id="home">
            <Hero />
            <Projects />
            <About />
        </main>
    <Footer/>
</template>

<style scoped>

</style>
