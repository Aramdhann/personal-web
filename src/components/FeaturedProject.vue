<script setup>
import FeaturedProjectItem from "@/components/FeaturedProjectItem.vue";
import Header from "@/components/Header.vue";
import projects from "@/data/project-data.json";
</script>

<template>
  <section class="container">
    <Header :seeAllLink="'/portofolio'" :seeAllText="'See All Project'">
      <template #title>Featured Projects</template>
    </Header>
    <div class="project-list">
      <FeaturedProjectItem :items="projects" :limit="4" />
    </div>
  </section>
</template>
