<script setup lang="ts">
import type { Project } from "@@/types/project";

const projects: Project[] = [
  { slug: "project-one", title: "Project One", tag: "Drop 01", cover: "" },
  { slug: "project-two", title: "Project Two", tag: "Drop 02", cover: "" },
  { slug: "project-three", title: "Project Three", tag: "Drop 03", cover: "" },
  { slug: "project-four", title: "Project Four", tag: "Drop 04", cover: "" },
];

useHead({ title: "Projects — ROCKASHAKA" });
</script>

<template>
  <SectionBlock eyebrow="Projects" title="All Drops">
    <ProjectsGrid :projects="projects" />
  </SectionBlock>
</template>
