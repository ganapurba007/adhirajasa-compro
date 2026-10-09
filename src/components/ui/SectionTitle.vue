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
    <!-- Badge Subtitle -->
    <div 
      v-if="badge"
      class="inline-flex items-center gap-2 px-3 py-1 rounded-md text-xs font-bold uppercase tracking-wider mb-3"
      :class="[
        dark 
          ? 'bg-amber-400/10 text-amber-400 border border-amber-400/20' 
          : 'bg-amber-500/10 text-amber-600 border border-amber-500/20'
      ]"
    >
      <span class="w-1.5 h-1.5 rounded-full bg-amber-500"></span>
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
