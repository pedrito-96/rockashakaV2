<script setup lang="ts">
const nav = [
  { to: '/', label: 'Home' },
  { to: '/about', label: 'About' },
  { to: '/projects', label: 'Projects' },
  { to: '/shop', label: 'Shop' },
  { to: '/contact', label: 'Contact' },
]
</script>

<template>
  <header class="sticky top-0 z-50 bg-white/80 backdrop-blur border-b border-black/10">
    <div class="mx-auto max-w-7xl px-6 h-16 flex items-center justify-between">
      <NuxtLink to="/" class="font-bold tracking-tight text-xl">
        ROCKASHAKA
      </NuxtLink>
      <nav class="flex gap-6 text-sm">
        <NuxtLink
          v-for="item in nav"
          :key="item.to"
          :to="item.to"
          class="hover:underline"
        >
          {{ item.label }}
        </NuxtLink>
      </nav>
    </div>
  </header>
</template>
