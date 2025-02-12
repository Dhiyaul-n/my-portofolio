<script setup>
import { ref, onMounted } from "vue";
import { gsap } from "gsap";

// Form Data
const name = ref("");
const email = ref("");
const message = ref("");

// GSAP Animations on Mount
onMounted(() => {
    gsap.from(".contact-heading", {
        opacity: 0,
        y: -50,
        duration: 1,
        ease: "power2.out",
    });

    gsap.from(".contact-form", {
        opacity: 0,
        x: -100,
        duration: 1,
        delay: 0.5,
        ease: "power2.out",
    });

    gsap.from(".contact-socials", {
        opacity: 0,
        x: 100,
        duration: 1,
        delay: 1,
        ease: "power2.out",
    });
});

// Submit Function (Can be replaced with actual API call)
const submitForm = () => {
    alert(`Message sent by ${name.value}!`);
};
</script>

<template>
    <div
        class="flex flex-col items-center justify-center min-h-screen bg-gradient-to-b from-[#0e233b] to-[#004D7A] text-white px-6">

        <!-- Heading -->
        <h1 class="text-3xl md:text-5xl font-bold mb-6 contact-heading">Contact Me</h1>

        <!-- Profile Card -->
        <div
            class="profile-card bg-white/10 backdrop-blur-lg p-6 md:p-8 rounded-2xl shadow-lg w-full max-w-sm text-center text-white transition-transform duration-300 transform hover:scale-105">

            <!-- Profile Picture -->
            <div
                class="profile-img mx-auto w-28 h-28 md:w-32 md:h-32 rounded-full overflow-hidden">
                <img src="../assets/img/profile.jpg" alt="Profile Picture" class="w-full h-full object-cover" />
            </div>

            <!-- Profile Info -->
            <h2 class="text-2xl font-bold mt-4 profile-text">Dhiyaul Nawaz J</h2>
            <p class="text-gray-300 text-sm profile-text">Web Developer | Student</p>

            <div class="mt-4 text-sm space-y-3">
                <p class="flex items-center justify-center space-x-2 text-gray-200 profile-text">
                    📍 <span>Tasikmalaya, Jawa Barat, Indonesia</span>
                </p>
                <p class="flex items-center justify-center space-x-2 text-gray-200 profile-text">
                    🎓 <span>SMKN 4 TASIKMALAYA</span>
                </p>
                <p class="flex items-center justify-center space-x-2 text-gray-200 profile-text">
                    ✉️ <a href="mailto:dhiyauln@gmail.com" class="text-blue-400 hover:underline">dhiyaulnawazjannan@gmail.com</a>
                </p>
            </div>
        </div>

            <!-- Social Links -->
            <div class="flex space-x-6 mt-6 contact-socials">

                <!-- GitHub -->
                <a href="https://github.com/Dhiyaul-n" target="_blank" class="hover:scale-110 transition-transform">
                    <svg class="w-6 h-6 transition-transform duration-300 group-hover:scale-125" fill="white"
                        viewBox="0 0 24 24">
                        <path fill-rule="evenodd"
                            d="M12 0C5.373 0 0 5.373 0 12c0 5.303 3.438 9.8 8.207 11.387.6.111.793-.26.793-.577v-2.172c-3.338.726-4.043-1.416-4.043-1.416-.546-1.387-1.334-1.757-1.334-1.757-1.09-.745.083-.73.083-.73 1.205.083 1.839 1.237 1.839 1.237 1.07 1.832 2.805 1.303 3.49.996.108-.775.418-1.304.76-1.604-2.665-.305-5.467-1.332-5.467-5.93 0-1.31.468-2.38 1.236-3.22-.124-.303-.536-1.526.117-3.176 0 0 1.008-.322 3.3 1.23a11.502 11.502 0 013.003-.404c1.018.005 2.045.138 3.002.404 2.292-1.552 3.3-1.23 3.3-1.23.653 1.65.24 2.873.117 3.176.77.84 1.236 1.91 1.236 3.22 0 4.61-2.805 5.625-5.475 5.92.43.372.812 1.102.812 2.222v3.293c0 .32.19.693.8.576C20.565 21.795 24 17.298 24 12c0-6.627-5.373-12-12-12z">
                        </path>
                    </svg>
                </a>

                <!-- Instagram -->
                <a href="https://instagram.com/dhiyauru" target="_blank" class="hover:scale-110 transition-transform">
                    <svg class="w-6 h-6 transition-transform duration-300 group-hover:scale-125" fill="white"
                        viewBox="0 0 24 24">
                        <path
                            d="M7.75 2C4.574 2 2 4.574 2 7.75v8.5C2 19.426 4.574 22 7.75 22h8.5C19.426 22 22 19.426 22 16.25v-8.5C22 4.574 19.426 2 16.25 2h-8.5zM12 6.25a5.75 5.75 0 110 11.5 5.75 5.75 0 010-11.5zM12 8a4 4 0 100 8 4 4 0 000-8zm5.75-.5a1.25 1.25 0 100 2.5 1.25 1.25 0 000-2.5z">
                        </path>
                    </svg> </a>

                <!-- LinkedIn -->
                <a href="https://www.linkedin.com/in/dhiyaul-nawaz-janan-863507330/" target="_blank"
                    class="hover:scale-110 transition-transform">
                    <svg class="w-6 h-6 transition-transform duration-300 group-hover:scale-125" fill="white"
                        viewBox="0 0 24 24">
                        <path
                            d="M20.452 20.452h-3.631v-5.569c0-1.327-.028-3.038-1.85-3.038-1.852 0-2.136 1.445-2.136 2.938v5.669H9.206V9.78h3.488v1.453h.05c.487-.921 1.676-1.89 3.447-1.89 3.688 0 4.371 2.429 4.371 5.594v5.515zM5.337 8.325a2.1 2.1 0 11-.002-4.2 2.1 2.1 0 01.002 4.2zM7.153 20.452H3.522V9.78h3.631v10.672z">
                        </path>
                    </svg> </a>

            </div>
        </div>
</template>
