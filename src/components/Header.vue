<template>
    <header class="fixed top-0 left-0 w-full p-3 flex justify-between items-center z-50 bg-primary shadow-md">
        <!-- Logo -->
        <div class="w-12 h-12 md:w-16 md:h-16 flex items-center justify-center">
            <img src="../assets/img/Logo.png" alt="Logo Marca Luis Medina" >
        </div>

        <!-- Navegación Principal -->
        <nav :class="`text-center sm:flex ${isMenuOpen ? 'block' : 'hidden'} absolute sm:static top-16 left-0 w-full sm:w-auto bg-primary sm:bg-transparent shadow-md sm:shadow-none` ">
            <ul class=" flex flex-col sm:flex-row sm:space-x-6 space-y-3 sm:space-y-0 text-lg font-medium p-4 sm:p-0">
                <li><a href="#" class="hover:text-accent">Sobre mí</a></li>
                <li><a href="#" class="hover:text-accent">Proyectos</a></li>
                <li><a href="#" class="hover:text-accent">Contacto</a></li>
            </ul>
        </nav>

        <!-- Botón de navegación móvil -->
        <div class="sm:hidden">
            <button @click="toggleMenu" class="focus:outline-none">
                <Menu v-if="!isMenuOpen" class="h-8 w-8" />
                <X v-else class="h-8 w-8" />
            </button>
        </div>
    </header>
</template>

<script setup>
import { ref } from 'vue';
import { AlignCenter, Menu, X } from 'lucide-vue-next';

// Estado para controlar si el menú está abierto o cerrado
const isMenuOpen = ref(false);

// Función para alternar el estado del menú
const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
};
</script>

<style scoped>
/* Puedes agregar estilos adicionales si es necesario */
</style>