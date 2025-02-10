<template>
    <header class="bg-gray-800 text-white py-4 px-6">
        <div class="container mx-auto flex justify-between items-center">
            <!-- Logo -->
            <h1
                class="text-lg font-bebasneue font-serif bg-gradient-to-r from-white to-black bg-[length:200%_100%] bg-clip-text text-transparent glow-effect">
                <NuxtLink to="/">Dhiyaul-n</NuxtLink>
            </h1>


            <nav class="hidden md:flex space-x-6">
                <!-- Desktop Links -->
                <NuxtLink to="/" class="px-4 py-2 rounded-lg transition duration-300 
                    relative inline-block hover:bg-[#52677D]/30 hover:text-[#facc15] 
                    border-b-2 border-transparent 
                    dark:text-white dark:hover:border-yellow-400 dark:hover:text-yellow-400" :class="{
                        'bg-[#52677D]/10 text-white': route.path === '/',
                        'border-yellow-400': selectedLink === '/',
                    }" @click="selectLink('/')">
                    Home
                </NuxtLink>

                <NuxtLink to="/about" class="px-4 py-2 rounded-lg transition duration-300 
                    relative inline-block hover:bg-[#52677D]/30 hover:text-[#facc15] 
                    border-b-2 border-transparent 
                    dark:text-white dark:hover:border-yellow-400 dark:hover:text-yellow-400" :class="{
                        'bg-[#52677D]/10 text-white': route.path === '/about',
                        'border-yellow-400': selectedLink === '/about',
                    }" @click="selectLink('/about')">
                    About
                </NuxtLink>

                <NuxtLink to="/projects" class="px-4 py-2 rounded-lg transition duration-300 
                    relative inline-block hover:bg-[#52677D]/30 hover:text-[#facc15] 
                    border-b-2 border-transparent 
                    dark:text-white dark:hover:border-yellow-400 dark:hover:text-yellow-400" :class="{
                        'bg-[#52677D]/10 text-white': route.path === '/projects',
                        'border-yellow-400': selectedLink === '/projects',
                    }" @click="selectLink('/projects')">
                    Projects
                </NuxtLink>

                <NuxtLink to="/contact" class="px-4 py-2 rounded-lg transition duration-300 
                    relative inline-block hover:bg-[#52677D]/30 hover:text-[#facc15] 
                    border-b-2 border-transparent 
                    dark:text-white dark:hover:border-yellow-400 dark:hover:text-yellow-400" :class="{
                        'bg-[#52677D]/10 text-white': route.path === '/contact',
                        'border-yellow-400': selectedLink === '/contact',
                    }" @click="selectLink('/contact')">
                    Contact
                </NuxtLink>
            </nav>

            <!-- Hamburger Button (Mobile) -->
            <button class="md:hidden flex flex-col space-y-1.5 z-50" @click="toggleMenu">
                <div class="h-1 w-6 bg-white rounded transition-transform duration-300"
                    :class="{ 'rotate-45 translate-y-2': menuOpen }"></div>
                <div class="h-1 w-6 bg-white rounded transition-opacity duration-300"
                    :class="{ 'opacity-0': menuOpen }"></div>
                <div class="h-1 w-6 bg-white rounded transition-transform duration-300"
                    :class="{ '-rotate-45 -translate-y-2': menuOpen }"></div>
            </button>
        </div>

        <!-- Mobile Menu (Vertical Layout) -->
        <div class="fixed inset-0 bg-black/50 z-40 transition-opacity duration-300"
            :class="{ 'opacity-100 pointer-events-auto': menuOpen, 'opacity-0 pointer-events-none': !menuOpen }"
            @click="menuOpen = false"></div>

        <div class="fixed top-0 right-0 w-64 h-full bg-gray-800 shadow-lg transform transition-transform duration-300 z-50"
            :class="{ 'translate-x-0': menuOpen, 'translate-x-full': !menuOpen }">
            <div class="p-6">
                <button class="absolute top-4 right-4 text-white text-xl grayscale-100 brightness-200" @click="menuOpen = false">✖</button>
                <nav class="mt-8 flex flex-col space-y-4">
                    <!-- Mobile Menu Items (Vertical) -->
                    <NuxtLink to="/"
                        class="px-4 py-2 rounded-lg hover:bg-[#52677D]/30 hover:text-[#facc15] transition duration-300"
                        :class="{ 'bg-[#52677D]/10 text-white': selectedLink === '/', 'border-b-2 border-yellow-400': selectedLink === '/' }"
                        @click="selectLink('/')">Home</NuxtLink>
                    <NuxtLink to="/about"
                        class="px-4 py-2 rounded-lg hover:bg-[#52677D]/30 hover:text-[#facc15] transition duration-300"
                        :class="{ 'bg-[#52677D]/10 text-white': selectedLink === '/about', 'border-b-2 border-yellow-400': selectedLink === '/about' }"
                        @click="selectLink('/about')">About</NuxtLink>
                    <NuxtLink to="/projects"
                        class="px-4 py-2 rounded-lg hover:bg-[#52677D]/30 hover:text-[#facc15] transition duration-300"
                        :class="{ 'bg-[#52677D]/10 text-white': selectedLink === '/projects', 'border-b-2 border-yellow-400': selectedLink === '/projects' }"
                        @click="selectLink('/projects')">Projects</NuxtLink>
                    <NuxtLink to="/contact"
                        class="px-4 py-2 rounded-lg hover:bg-[#52677D]/30 hover:text-[#facc15] transition duration-300"
                        :class="{ 'bg-[#52677D]/10 text-white': selectedLink === '/contact', 'border-b-2 border-yellow-400': selectedLink === '/contact' }"
                        @click="selectLink('/contact')">Contact</NuxtLink>
                </nav>
            </div>
        </div>
    </header>
</template>

<script setup>
// main.js or main.ts
import './assets/css/main.css';
import { useRoute } from "vue-router";
import { ref, onMounted } from "vue";
import gsap from "gsap";

// Get the current route
const route = useRoute();

// State for menu and selected link
const menuOpen = ref(false);
const selectedLink = ref(route.path);

// Toggle the mobile menu
const toggleMenu = () => {
    menuOpen.value = !menuOpen.value;
};

// Set the selected link
const selectLink = (path) => {
    selectedLink.value = path;
    menuOpen.value = false; // Close the menu after selecting a link
};



</script>

<style scoped>
.glow-effect {
    text-shadow: 0px 0px 2px rgba(255, 255, 255, 0.9),
        0px 0px 40px rgba(0, 0, 0, 0.7),
        0px 0px 30px rgba(0, 0, 0, 0.6);
}
</style>
