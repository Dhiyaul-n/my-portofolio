<template>
    <div class="min-h-screen bg-gradient-to-b from-[#0e233b] to-[#004D7A] py-12 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <h1 class="text-4xl text-white font-bold text-center mb-12">My Projects</h1>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-12">
                <!-- Project Card 1 -->
                <div
                    class="bg-[#1F2A44] p-6 rounded-lg shadow-lg transition-transform duration-300 hover:scale-105 hover:shadow-xl">
                    <img src="../assets/img/project1.png" alt="Project 1"
                        class="w-full h-48 object-cover rounded-md mb-6" />
                    <h2 class="text-xl text-white font-semibold mb-2">Perpus Digital</h2>
                    <p class="text-gray-300 mb-4 text-justify">Web Perpustakaan Digital adalah web perpustakaan sekolah untuk mempermudah akses buku, pencarian materi, layanan online, dan mencatat kunjungan siswa serta staf.</p>
                </div>

                <!-- Project Card 2 -->
                <div
                    class="bg-[#1F2A44] p-6 rounded-lg shadow-lg transition-transform duration-300 hover:scale-105 hover:shadow-xl">
                    <img src="../assets/img/project2.png" alt="Project 2"
                        class="w-full h-48 object-cover rounded-md mb-6" />
                    <h2 class="text-xl text-white font-semibold mb-2">Web Sekolah SMKN 4 TASIKMALAYA</h2>
                    <p class="text-gray-300 mb-4 text-justify">Website sekolah yang menampilkan profil sekolah, ruangan, fasilitas, informasi guru dan staf, serta statistik siswa untuk memberikan gambaran lengkap tentang institusi.</p>
                </div>

                <!-- Project Card 3 -->
            </div>
        </div>
    </div>
</template>

<script setup>
// You can add data or other logic for your projects here, or keep it static as shown.
</script>

<style scoped>
/* You can customize the card hover and scaling effects further */
.project-card:hover {
    transform: scale(1.05);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
}

.project-card .project-title {
    font-size: 1.25rem;
    font-weight: bold;
    color: #fff;
}

.project-card .project-description {
    font-size: 1rem;
    color: #ddd;
}
</style>
