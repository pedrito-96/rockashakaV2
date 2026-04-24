<script setup lang="ts">
import type { Project } from '~/types/project'

defineProps<{ projects: Project[] }>()
</script>

<template>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <ProjectCard
      v-for="p in projects"
      :key="p.slug"
      v-bind="p"
    />
  </div>
</template>
