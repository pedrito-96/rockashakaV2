<script setup lang="ts">
import type { Project } from "@@/types/project";

const featured: Project[] = [
  { slug: "project-one", title: "Project One", tag: "Drop 01", cover: "" },
  { slug: "project-two", title: "Project Two", tag: "Drop 02", cover: "" },
  { slug: "project-three", title: "Project Three", tag: "Drop 03", cover: "" },
];

useHead({ title: "ROCKASHAKA" });
</script>

<template>
  <div>
    <HeroSection
      title="ROCKASHAKA"
      subtitle="Sound, culture, and capsule drops. Concept in motion."
      :cta="{ label: 'Explore', to: '/projects' }"
    />

    <SectionBlock eyebrow="About" title="What we are">
      <p class="max-w-2xl text-lg opacity-80">
        Rockashaka builds raw, unpolished experiences — music, merch, and
        moments. Each drop tells its own story.
      </p>
    </SectionBlock>

    <SectionBlock eyebrow="Featured" title="Latest Drops">
      <ProjectsGrid :projects="featured" />
    </SectionBlock>

    <SectionBlock eyebrow="Contact" title="Say hi">
      <ContactForm />
    </SectionBlock>
  </div>
</template>
