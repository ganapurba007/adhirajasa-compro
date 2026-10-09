<script setup>
</script>

<template>
  <div class="min-h-[60vh] flex flex-col items-center justify-center py-20 px-4 text-center">
    <div class="text-7xl font-extrabold text-amber-500 mb-4">404</div>
    <h1 class="text-3xl font-bold text-slate-900 mb-2">Halaman Tidak Ditemukan</h1>
    <p class="text-slate-600 max-w-md mx-auto mb-8">
      Maaf, halaman yang Anda cari tidak tersedia atau telah dipindahkan.
    </p>
    <router-link
      to="/"
      class="inline-flex items-center justify-center px-6 py-3 rounded-lg bg-slate-900 hover:bg-slate-800 text-white font-semibold transition duration-200"
    >
      Kembali ke Beranda
    </router-link>
  </div>
</template>
