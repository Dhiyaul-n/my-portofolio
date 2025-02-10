<template>
    <div class="min-h-screen bg-gradient-to-b from-[#0e233b] to-[#004D7A] text-white flex flex-col items-center px-4 sm:px-6 md:px-12">
        <!-- Profile Card -->
        <div
            class="bg-black-800/20 p-16 rounded-2xl shadow-lg flex flex-col md:flex-row items-center self-center justify-center md:items-start w-full max-w-[90%] md:max-w-[70%] transition-transform duration-500 hover:scale-105 hover:shadow-xl hover:rounded-2xl animate-fadeIn mt-10 mb-10">

            <!-- Profile Image -->
            <img src="assets/img/profile.jpg" alt="Profile Picture"
                class="w-32 h-32 sm:w-36 sm:h-36 md:w-60 md:h-60 rounded-full object-cover shadow-lg mb-4 md:mb-0 md:mr-6 animate-fadeIn delay-200 transition-transform duration-500 ease-in-out hover:rotate-360 mx-auto" />

            <!-- Text Section -->
            <div class="flex flex-col text-center md:text-left animate-fadeIn delay-400 w-full">
                <h1 class="text-3xl sm:text-4xl md:text-5xl font-bold mb-4">About Me</h1>
                <h2 class="text-xl md:text-2xl font-semibold text-yellow-400">Dhiyaul Nawaz J</h2>
                <p class="text-base sm:text-lg md:text-xl text-gray-300"> Web Developer & Student</p>
                <p
                    class="text-sm sm:text-lg text-justify text-gray-300 mt-4 leading-relaxed max-w-[90%] md:max-w-[80%] mx-auto md:mx-0">
                    Hello! I'm <span class="text-yellow-400 font-semibold">Dhiyaul Nawaz J</span>, a passionate web
                    developer who loves building interactive and dynamic websites. I specialize in modern JavaScript
                    frameworks like Vue.js & Nuxt.js. I am always looking for new challenges and opportunities to grow
                    as a developer.
                </p>
            </div>
        </div>

        <!-- Skills Section -->
        <div
            class="mt-8 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 animate-fadeIn delay-300 w-full max-w-[90%] md:max-w-[70%]">
            <!-- Skill Cards (SVGs Unchanged) -->
            <div
                class="skill-card bg-black/10 p-4 rounded-lg shadow-md flex flex-col items-center transition-transform ease-in-out transform hover:scale-110 hover:shadow-xl duration-600">
                <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 50 50">
                    <path
                        d="M 45.273438 2.324219 C 45.085938 2.117188 44.816406 2 44.535156 2 L 5.464844 2 C 5.183594 2 4.914063 2.117188 4.726563 2.324219 C 4.535156 2.53125 4.441406 2.808594 4.46875 3.089844 L 7.988281 42.515625 C 8.023438 42.929688 8.3125 43.273438 8.710938 43.390625 L 24.722656 47.960938 C 24.808594 47.988281 24.902344 48 24.996094 48 C 25.089844 48 25.179688 47.988281 25.269531 47.960938 L 41.292969 43.390625 C 41.691406 43.273438 41.976563 42.929688 42.015625 42.515625 L 45.53125 3.089844 C 45.558594 2.808594 45.464844 2.53125 45.273438 2.324219 Z M 36.847656 15.917969 L 18.035156 15.917969 L 18.484375 21.007813 L 36.394531 21.007813 L 35.050781 36.050781 L 24.992188 39.089844 L 24.894531 39.058594 L 14.953125 36.046875 L 14.410156 29.917969 L 19.28125 29.917969 L 19.492188 32.296875 L 25.050781 33.460938 L 30.507813 32.296875 L 31.089844 25.859375 L 14.046875 25.859375 L 12.722656 11.054688 L 37.28125 11.054688 Z">
                    </path>
                </svg> <span class="text-white font-semibold">HTML</span>
            </div>

            <div
                class="skill-card bg-black/10 p-4 rounded-lg shadow-md flex flex-col items-center transition-transform ease-in-out transform hover:scale-110 hover:shadow-xl duration-600">
                <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 48 48">
                    <linearGradient id="TQDriqswrKwPOniLrPT12a_7gdY5qNXaKC0_gr1" x1="16.33" x2="32.293" y1="-2.748"
                        y2="41.109" gradientUnits="userSpaceOnUse">
                        <stop offset="0" stop-color="#2aa4f4"></stop>
                        <stop offset="1" stop-color="#007ad9"></stop>
                    </linearGradient>
                    <path fill="url(#TQDriqswrKwPOniLrPT12a_7gdY5qNXaKC0_gr1)"
                        d="M7.192,7.176l2.627,29.77c0.109,1.237,0.97,2.28,2.164,2.621l10.643,3.041	c0.898,0.257,1.849,0.257,2.747,0l10.643-3.041c1.194-0.341,2.055-1.383,2.164-2.621l2.627-29.77C40.911,6.006,39.99,5,38.816,5	H9.184C8.01,5,7.089,6.006,7.192,7.176z">
                    </path>
                    <path fill="#35c1f1"
                        d="M24,8v31.9l9.876-2.822c0.797-0.228,1.371-0.924,1.443-1.749l2.286-26.242	C37.656,8.502,37.196,8,36.609,8H24z">
                    </path>
                    <path fill="#fff"
                        d="M33.1,13H24v4h4.9l-0.3,4H24v4h4.4l-0.3,4.5L24,30.9v4.2l7.9-2.6L32.6,21l0,0L33.1,13z"></path>
                    <path fill="#d6e0e9"
                        d="M24,13v4h-8.9l-0.3-4H24z M19.4,21l0.2,4H24v-4H19.4z M19.8,27h-4l0.3,5.5l7.9,2.6v-4.2l-4.1-1.4	L19.8,27z">
                    </path>
                    <path
                        d="M33.1,13l-0.5,8l-0.7,11.5L24,35.1l-7.9-2.6L15.8,27h4l0.1,2.5l4.1,1.4l4.1-1.4l0.3-4.5H24h-4.4l-0.2-4H24h4.6l0.3-4H24 h-8.9l-0.3-4H24H33.1 M34.164,12H33.1H24h-9.2h-1.078l0.081,1.075l0.3,4L14.172,18H15.1H24h3.822l-0.15,2H24h-4.6h-1.051 l0.052,1.05l0.2,4L18.649,26H15.8h-1.056l0.058,1.054l0.3,5.5l0.037,0.682l0.649,0.214l7.9,2.6L24,36.153l0.313-0.103l7.9-2.6 l0.644-0.212l0.041-0.677l0.7-11.5l0.5-7.998L34.164,12L34.164,12z M20.761,26H24h3.331l-0.185,2.769L24,29.843l-3.128-1.068 l-0.073-1.815L20.761,26L20.761,26z"
                        opacity=".05"></path>
                    <path
                        d="M33.1,13l-0.5,8l-0.7,11.5L24,35.1l-7.9-2.6L15.8,27h4l0.1,2.5l4.1,1.4l4.1-1.4l0.3-4.5H24h-4.4l-0.2-4H24h4.6l0.3-4H24 h-8.9l-0.3-4H24H33.1 M33.632,12.5H33.1H24h-9.2h-0.539l0.04,0.537l0.3,4l0.035,0.463H15.1H24h4.361l-0.225,3H24h-4.6h-0.526 l0.026,0.525l0.2,4l0.024,0.475H19.6H24h3.866l-0.242,3.634L24,30.372l-3.614-1.234L20.3,26.98L20.28,26.5H19.8h-4h-0.528 l0.029,0.527l0.3,5.5l0.019,0.341l0.324,0.107l7.9,2.6L24,35.626l0.156-0.051l7.9-2.6l0.322-0.106l0.021-0.339l0.7-11.5l0.5-7.999 L33.632,12.5L33.632,12.5z"
                        opacity=".07"></path>
                </svg> <span class="text-white font-semibold">CSS</span>
            </div>

            <div
                class="skill-card bg-black/10 p-4 rounded-lg shadow-md flex flex-col items-center transition-transform ease-in-out transform hover:scale-110 hover:shadow-xl duration-600">
                <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="100" height="100" viewBox="0 0 48 48">
                    <path fill="#ffd600" d="M6,42V6h36v36H6z"></path>
                    <path fill="#000001"
                        d="M29.538 32.947c.692 1.124 1.444 2.201 3.037 2.201 1.338 0 2.04-.665 2.04-1.585 0-1.101-.726-1.492-2.198-2.133l-.807-.344c-2.329-.988-3.878-2.226-3.878-4.841 0-2.41 1.845-4.244 4.728-4.244 2.053 0 3.528.711 4.592 2.573l-2.514 1.607c-.553-.988-1.151-1.377-2.078-1.377-.946 0-1.545.597-1.545 1.377 0 .964.6 1.354 1.985 1.951l.807.344C36.452 29.645 38 30.839 38 33.523 38 36.415 35.716 38 32.65 38c-2.999 0-4.702-1.505-5.65-3.368L29.538 32.947zM17.952 33.029c.506.906 1.275 1.603 2.381 1.603 1.058 0 1.667-.418 1.667-2.043V22h3.333v11.101c0 3.367-1.953 4.899-4.805 4.899-2.577 0-4.437-1.746-5.195-3.368L17.952 33.029z">
                    </path>
                </svg> <span class="text-white font-semibold">JS</span>
            </div>
        </div>

        <!-- Education Section -->
        <div
            class="bg-black/10 p-6 rounded-lg shadow-lg transition-transform duration-300 hover:scale-105 hover:shadow-xl mt-10 mb-10 w-full max-w-[90%] md:max-w-[70%]">
            <div class="flex flex-row items-center mb-6">
                <!-- Logo -->
                <div class="w-20 h-20 md:w-16 md:h-16 rounded-full flex items-center justify-center mb-4 md:mb-0 mr-4">
                    <img src="../assets/img/logosmk.png" alt="SMKN 4 TASIKMALAYA Logo"
                        class="w-full h-full object-contain rounded-full" />
                </div>

                <!-- Text Section -->
                <div class="text-center md:text-left">
                    <h2 class="lg:text-3xl sm:text-[20px] text-white font-semibold mb-2">SMKN 4 TASIKMALAYA</h2>
                    <p class="text-gray-300 lg-:text-xl sm:text-sm">Computer Science</p>
                </div>
            </div>

            <!-- Timeline -->
            <div class="flex flex-col md:flex-row justify-between items-center text-sm text-gray-400">
                <div>
                    <p class="font-medium text-white">Start Date : <span class="text-gray-300">October 2022</span></p>
                    <p class="font-medium text-white">Expected Graduation : <span class="text-gray-300">-</span></p>
                </div>
            </div>
        </div>

        <div class="flex justify-center items-center p-4 py-30 ">
            <div ref="card" class="w-96 h-40 text-white flex items-center justify-center 
                shadow-xl rounded-lg">
                <img class="rounded-2xl " src="../assets/img/GGJ.png" alt="">
            </div>
        </div>


        <!-- Contact Button -->
        <NuxtLink to="/contact"
            class="mt-4 mb-8 bg-yellow-400 text-gray-900 px-6 py-2 sm:px-4 sm:py-1 rounded-md font-semibold transition-all duration-300 ease-in-out hover:bg-yellow-500 hover:scale-105 hover:shadow-lg active:scale-95 animate-[fadeIn_1s_ease-out_forwards] w-xs sm:w-auto text-center">
            Contact Me
        </NuxtLink>



    </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import gsap from "gsap";


const card = ref(null);

onMounted(() => {
    if (!card.value) return;

    card.value.addEventListener("mousemove", (e) => {
        const { offsetWidth, offsetHeight } = card.value;
        const { offsetX, offsetY } = e;

        const rotateX = ((offsetY / offsetHeight) - 0.5) * 40; // Max 20deg
        const rotateY = ((offsetX / offsetWidth) - 0.5) * -40; // Max -20deg

        // Use GSAP for smooth movement
        gsap.to(card.value, {
            rotationX: rotateX,
            rotationY: rotateY,
            transformPerspective: 1000,
            ease: "power2.out",
            duration: 0.3,
        });
    });

    card.value.addEventListener("mouseleave", () => {
        // Smoothly reset to original position
        gsap.to(card.value, {
            rotationX: 0,
            rotationY: 0,
            transformPerspective: 1000,
            ease: "power2.out",
            duration: 0.5,
        });
    });
});



</script>

<style scoped>
/* Fade In Animation */
@keyframes fadeIn {
    0% {
        opacity: 0;
    }

    100% {
        opacity: 1;
    }
}

.animate-fadeIn {
    animation: fadeIn 1s ease-in-out forwards;
}
</style>
