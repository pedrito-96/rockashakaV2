<script setup lang="ts">
defineProps<{
  title?: string
  eyebrow?: string
}>()
</script>

<template>
  <section class="py-24">
    <div class="mx-auto max-w-7xl px-6">
      <p v-if="eyebrow" class="text-sm uppercase tracking-widest opacity-60 mb-3">
        {{ eyebrow }}
      </p>
      <h2 v-if="title" class="text-4xl md:text-5xl font-bold mb-10">
        {{ title }}
      </h2>
      <slot />
    </div>
  </section>
</template>
