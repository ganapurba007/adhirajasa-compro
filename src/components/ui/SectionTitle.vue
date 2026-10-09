<script setup>
defineProps({
  badge: {
    type: String,
    default: ''
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    default: ''
  },
  align: {
    type: String,
    default: 'left',
    validator: (v) => ['left', 'center', 'right'].includes(v)
  },
  dark: {
    type: Boolean,
    default: false
  }
})
</script>

<template>
  <div 
    class="mb-10 lg:mb-14"
    :class="[
      align === 'center' ? 'text-center mx-auto max-w-3xl' : align === 'right' ? 'text-right' : 'text-left max-w-2xl'
    ]"
  >
    <!-- Category Eyebrow (Clean Non-Badge Style) -->
    <div 
      v-if="badge"
      class="text-xs font-extrabold uppercase tracking-widest mb-3 flex items-center gap-2"
      :class="[
        align === 'center' ? 'justify-center' : align === 'right' ? 'justify-end' : 'justify-start',
        dark ? 'text-amber-400' : 'text-amber-600'
      ]"
    >
      <span class="w-4 h-0.5 rounded-full" :class="dark ? 'bg-amber-400' : 'bg-amber-500'"></span>
      <span>{{ badge }}</span>
    </div>

    <!-- Main Title Heading -->
    <h2 
      class="text-2xl sm:text-3xl lg:text-4xl font-extrabold tracking-tight leading-tight"
      :class="[dark ? 'text-white' : 'text-slate-900']"
    >
      {{ title }}
    </h2>

    <!-- Description -->
    <p 
      v-if="description"
      class="mt-4 text-base sm:text-lg leading-relaxed"
      :class="[dark ? 'text-slate-300' : 'text-slate-600']"
    >
      {{ description }}
    </p>
  </div>
</template>
