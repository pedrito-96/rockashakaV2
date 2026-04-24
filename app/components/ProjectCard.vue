<script setup lang="ts">
defineProps<{
  slug: string
  title: string
  cover?: string
  tag?: string
}>()
</script>

<template>
  <NuxtLink
    :to="`/projects/${slug}`"
    class="group block"
  >
    <div class="aspect-[4/5] bg-neutral-200 overflow-hidden mb-3">
      <NuxtImg
        v-if="cover"
        :src="cover"
        :alt="title"
        class="w-full h-full object-cover group-hover:scale-105 transition duration-500"
      />
    </div>
    <p v-if="tag" class="text-xs uppercase tracking-widest opacity-60">{{ tag }}</p>
    <h3 class="text-lg font-semibold">{{ title }}</h3>
  </NuxtLink>
</template>
