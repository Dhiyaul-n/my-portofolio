<template>
    <div class="flex justify-center items-center min-h-screen bg-[#1a1a1a] p-4">
        <!-- Vinyl Player Card -->
        <div class="relative bg-[#222] p-6 rounded-3xl shadow-2xl w-full max-w-sm sm:max-w-md border-4 border-gray-700">
            <!-- Player Controls -->
            <div class="absolute top-3 left-3 flex space-x-2">
                <div class="w-3 h-3 bg-red-500 rounded-full animate-pulse"></div>
                <div class="w-3 h-3 bg-yellow-500 rounded-full"></div>
                <div class="w-3 h-3 bg-green-500 rounded-full"></div>
            </div>

            <!-- Vinyl Record -->
            <div class="flex justify-center mt-6 relative">
                <div
                    class="relative w-40 h-40 sm:w-48 sm:h-48 rounded-full bg-black/80 border-2 shadow-white/50 shadow-sm">
                    <!-- Spinning Vinyl with Profile Image -->
                    <div ref="vinyl" class="absolute inset-0 flex items-center justify-center">
                    </div>

                    <!-- Center Image (Remains Static) -->
                    <div class="absolute inset-0 flex items-center justify-center">
                        <div class="w-14 h-14 sm:w-16 sm:h-16 rounded-full border-1 border-white/10 overflow-hidden">
                            <img ref="vinyl" src="../assets/img/profile.jpg" alt="Album Cover"
                                class="w-full h-full object-cover">
                        </div>
                    </div>
                </div>

                <!-- Tonearm (Needle) -->
                <div class="absolute right-[-40px] top-[-20px] w-24 h-32">
                    <!-- Arm -->
                    <div ref="tonearm" class="absolute w-2 h-28 md:h-32 bg-gray-500 left-2 top-0 origin-top-left"></div>
                    <!-- Needle Head -->
                    <div class="absolute w-4 h-6 bg-gray-400 rounded-b-lg left-0 top-[112.5px] md:top-[128px]"></div>
                </div>
            </div>

            <!-- Title -->
            <div class="text-center mt-6">
                <h2 class="text-xl text-white font-bold">Dhiyaul Nawaz J</h2>
                <p class="text-sm text-gray-400">Web Developer, Student</p>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import gsap from "gsap";

// References for animation
const vinyl = ref(null);
const tonearm = ref(null);

onMounted(() => {
    // Vinyl spinning animation
    gsap.to(vinyl.value, {
        rotate: 360,
        duration: 5,
        ease: "linear",
        repeat: -1
    });

    // Adjust tonearm rotation based on screen size
    gsap.matchMedia().add("(max-width: 640px)", () => {
        // Mobile view (width <= 640px)
        gsap.to(tonearm.value, {
            rotate: 20, // Rotate to 40° in mobile
            transformOrigin: "top left",
            duration: 2,
            delay: 1,
            ease: "power2.inOut"
        });
    }).add("(min-width: 641px)", () => {
        // Desktop view (width > 640px)
        gsap.to(tonearm.value, {
            rotate: 32, // Rotate to 30° in larger screens
            transformOrigin: "top left",
            duration: 2,
            delay: 1,
            ease: "power2.inOut"
        });
    });
});
</script>

<style scoped>
/* Vinyl Player Shadow Effect */
.shadow-2xl {
    box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.5);
}
</style>