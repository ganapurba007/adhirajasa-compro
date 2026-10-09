<script setup>
import { useRoute } from 'vue-router'

const route = useRoute()
</script>

<template>
  <div class="max-w-7xl mx-auto px-4 py-16">
    <h1 class="text-3xl sm:text-4xl font-bold text-slate-900 mb-6">Detail Proyek</h1>
    <p class="text-slate-600 leading-relaxed">
      Menampilkan detail proyek: <span class="font-mono text-amber-600">{{ route.params.slug }}</span>
    </p>
  </div>
</template>
