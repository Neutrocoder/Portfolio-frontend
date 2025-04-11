<template>
    <section id="proyectos" class="text-light">
        <div class="container mx-auto text-center max-w-7xl px-6">
            <h2 class="text-4xl font-extrabold mb-15">Proyectos</h2>
            <div class="flex flex-col gap-8">
                <!-- card -->
                <div v-for="(project, index) in projects" :key="index" 
                    class="flex flex-col md:flex-row items-center  gap-6 p-6 rounded-3xl">
                    
                    <!-- Imagen -->
                    <img :src="project.image" :alt="project.name" 
                        class="w-full md:w-1/3 h-auto rounded-xl" />
                    
                    <!-- Contenido -->
                    <div class="text-center md:text-left w-full md:w-2/3">
                        <h3 class="text-3xl font-semibold mb-6">{{ project.name }}</h3>
                        <p class="text-gray-300 mb-4 max-w-xl mx-auto md:mx-0">{{ project.description }}</p>
                        <!-- bagde -->
                        <div class="flex flex-wrap justify-center sm:justify-start gap-2 mb-4">
                            <span 
                                v-for="(tech, i) in project.technologies" 
                                :key="i" 
                                class="px-3 py-1 text-sm font-medium bg-gray-800 text-gray-200 rounded-lg">
                                {{ tech }}
                            </span>
                        </div>
                        <!-- Botones -->
                        <div class="flex gap-4 justify-center md:justify-start">
                            <a :href="project.link" class="px-6 py-3 bg-secondary text-white rounded-xl flex items-center gap-2 transition-transform transform hover:scale-105">
                                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-github"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/><path d="M9 18c-4.51 2-5-2-7-2"/></svg>
                                Code
                            </a>
                            <a :href="project.preview" class="px-6 py-3 bg-accent text-white rounded-xl flex items-center gap-2 transition-transform transform hover:scale-105">
                                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"/><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"/></svg>
                                Preview
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>




<script >

export default {
    data() {
        return {
            projects: [
                {
                    name: 'EasyBank',
                    description: 'Landing page para un banco digital, con diseño moderno y responsive.',
                    image: 'src/assets/img/easybank.png',
                    link: '#',
                    preview: '#',
                    technologies: ['Vue', 'Tailwind',],
                },
                {
                    name: 'Bookmark',
                    description: 'Landing Page de Aplicación para guardar y organizar enlaces web de manera sencilla.',
                    image: 'src/assets/img/bookmark.png',
                    link: '#',
                    preview: '#',
                    technologies: ['Vue', 'Tailwind','Astro',],
                },
                {
                    name: 'Manage',
                    description: 'Landing Page de Herramienta de gestión de proyectos con tareas y seguimiento de progreso.',
                    image: 'src/assets/img/manage.png',
                    link: '#',
                    preview: '#',
                    technologies: ['Vue', 'Tailwind',],
                },
            ],
        };
    },
};
</script>

<style scoped>

</style>
