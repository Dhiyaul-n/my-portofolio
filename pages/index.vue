<template>
    <div class="container mx-auto bg-gradient-to-b from-[#0e233b] to-[#004D7A] min-w-full min-h-screen">
        <div class="flex justify-center items-center py-20 p-4">
            <!-- Vinyl Player Card -->
            <!-- Vinyl Player Card -->
            <div
                class="relative bg-[#222] opacity-90 p-6 rounded-3xl shadow-2xl w-full sm:max-w-xl lg:max-w-2xl xl:max-w-3xl border-2 border-gray-700">
                <!-- Player Controls -->
                <div class="absolute top-3 left-3 flex space-x-2">
                    <div class="w-3 h-3 bg-red-500 rounded-full animate-pulse"></div>
                    <div class="w-3 h-3 bg-yellow-500 rounded-full"></div>
                    <div class="w-3 h-3 bg-green-500 rounded-full"></div>
                </div>

                <!-- Vinyl Record -->
                <div class="flex justify-center mt-6 relative">
                    <div
                        class="relative w-40 h-40 sm:w-48 sm:h-48 md:w-80 md:h-80 rounded-full bg-black/80 border-1 border-white/20 shadow-white/50 shadow-sm">
                        <!-- Spinning Vinyl with Profile Image -->
                        <div ref="vinyl" class="absolute inset-0 flex items-center justify-center"></div>

                        <!-- Center Image (Remains Static) -->
                        <div class="absolute inset-0 flex items-center justify-center">
                            <div
                                class="w-14 h-14 md:w-32 md:h-32 rounded-full border-1 border-white/10 overflow-hidden ">
                                <img ref="vinyl" src="../assets/img/profile.jpg" alt="Album Cover"
                                    class="w-full h-full object-cover transform-gpu">
                            </div>
                        </div>
                    </div>

                    <!-- Tonearm (Needle) -->
                    <div class="absolute right-[-40px] top-[-20px] w-24 h-32 sm:w-28 sm:h-36 md:w-32 md:h-60">
                        <!-- Arm -->
                        <div ref="tonearm"
                            class="absolute w-1 md:w-2 h-28 sm:h-32 md:h-60 md:top-10 md:left-[-20px] bg-gray-500 left-2 top-5 origin-top-left">
                        </div>
                        <!-- Needle Head -->
                        <div
                            class="absolute w-2 md:w-4 h-3 md:h-6 bg-gray-400 rounded-b-lg left-1 md:left-[-28px] top-[130px] sm:top-[124px] md:top-[280px]">
                        </div>
                    </div>

                </div>

                <!-- Title (Perfectly Centered) -->
                <div class="flex flex-col items-center text-center mt-6">
                    <!-- GSAP Rolling Text Name -->
                    <h1 ref="rollingText"
                        class="bg-white/10 w-full max-w-xs text-center backdrop-brightness-200 brightness-200 rounded-lg font-thin text-white text-2xl sm:text-lg md:text-xl px-3 py-1 border-1 border-black/50">
                        <NuxtLink to="/" class="block text-black font-bebasneue font-semibold ">{{ displayText }}
                        </NuxtLink>
                    </h1>
                    <p class="text-sm text-gray-400 mt-3 b-0 tracking-wide hover:text-white ease-in-out duration-500 ">
                        Web
                        Developer | Student</p>
                </div>

                <div class="flex justify-center space-x-6 mt-6 contact-socials">

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
                    <a href="https://instagram.com/dhiyauru" target="_blank"
                        class="hover:scale-110 transition-transform">
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
        </div>

<!-- Education History -->
<div ref="educationSection" class="mt-10 mb-10 px-4">
  <h2 class="text-white text-xl md:text-2xl font-semibold border-b border-gray-600 pb-2 mb-4">
    Riwayat Pendidikan
  </h2>
  <ul class="space-y-4 text-gray-300 text-sm md:text-base">
    <li>
      <div class="flex flex-col md:flex-row md:justify-between">
        <span class="font-semibold text-white">SMK Negeri 4 Kota Tasikmalaya </span>
        <span class="text-gray-400">2022 - 2025</span>
      </div>
      <p class="text-gray-400">Rekayasa Perangkat Lunak</p>
    </li>
    <li>
      <div class="flex flex-col md:flex-row md:justify-between">
        <span class="font-semibold text-white">SMP Negeri 6 Kota Tasikmalaya </span>
        <span class="text-gray-400">2019 - 2022</span>
      </div>
    </li>
  </ul>
</div>




    </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import gsap from "gsap";


// Rolling text state
const finalText = "Dhiyaul Nawaz J";
const displayText = ref(finalText);
const rollingText = ref(null);
    const educationSection = ref(null);

onMounted(() => {
  gsap.from(educationSection.value, {
    opacity: 0,
    y: 50,
    duration: 1.2,
    delay: 1.5,
    ease: "power3.out"
  });
});


function startRolling() {
    let letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
    let index = 0;

    let timeline = gsap.timeline({ repeat: -1, repeatDelay: 2 });

    timeline.to({}, { duration: 1 }); // Initial delay

    for (let i = 0; i <= finalText.length; i++) {
        timeline.to({}, { duration: 0.1 }).call(() => {
            displayText.value = finalText
                .split("")
                .map((char, j) => (char === " " ? " " : j <= index ? finalText[j] : letters[Math.floor(Math.random() * letters.length)]))
                .join("");

            index++;
        });
    }
}

onMounted(() => {
    startRolling();
});


const vinyl = ref(null);
const tonearm = ref(null);

onMounted(() => {
    // Vinyl spinning animation
    gsap.to(vinyl.value, {
        rotate: 360,
        duration: 5,
        delay: 3,
        ease: "linear",
        repeat: -1
    });

    // Adjust tonearm rotation based on screen size
    gsap.matchMedia().add("(max-width: 640px)", () => {
        // Mobile view (width <= 640px)
        gsap.to(tonearm.value, {
            rotate: 20,
            transformOrigin: "top left",
            duration: 2,
            delay: 1,
            ease: "power2.inOut"
        });
    }).add("(min-width: 641px)", () => {
        // Desktop view (width > 640px)
        gsap.to(tonearm.value, {
            rotate: 32,
            transformOrigin: "top left",
            duration: 2,
            delay: 1,
            ease: "power2.inOut"
        });
    });
});



</script>


<style scoped></style>


