<script setup lang="ts">
defineProps<{
  title?: string
  subtitle?: string
  cta?: { label: string, to: string }
}>()
</script>

<template>
  <section class="relative min-h-[80vh] flex items-center justify-center overflow-hidden">
    <div class="absolute inset-0 bg-gradient-to-br from-black via-neutral-900 to-neutral-700" />
    <div class="relative z-10 text-center text-white px-6">
      <h1 class="text-6xl md:text-8xl font-black tracking-tight mb-6">
        {{ title ?? 'ROCKASHAKA' }}
      </h1>
      <p v-if="subtitle" class="text-lg md:text-xl opacity-80 max-w-2xl mx-auto mb-8">
        {{ subtitle }}
      </p>
      <NuxtLink
        v-if="cta"
        :to="cta.to"
        class="inline-block px-8 py-3 bg-white text-black font-semibold hover:bg-neutral-200 transition"
      >
        {{ cta.label }}
      </NuxtLink>
    </div>
  </section>
</template>
