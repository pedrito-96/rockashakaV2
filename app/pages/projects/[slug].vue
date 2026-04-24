<script setup lang="ts">
const route = useRoute()
const slug = route.params.slug as string

useHead({ title: `${slug} — ROCKASHAKA` })
</script>

<template>
  <SectionBlock :eyebrow="`Project`" :title="slug">
    <div class="max-w-3xl space-y-6 text-lg opacity-80">
      <div class="aspect-video bg-neutral-200 mb-8" />
      <p>Project detail placeholder for <strong>{{ slug }}</strong>.</p>
      <p>Replace with content from @nuxt/content or CMS.</p>
    </div>
  </SectionBlock>
</template>
