<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="min-h-screen flex flex-col bg-slate-50 text-slate-800">
    <main class="flex-grow">
      <RouterView />
    </main>
  </div>
</template>
