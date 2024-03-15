<script setup>
import FeaturedProjectItem from "@/components/FeaturedProjectItem.vue";
import Header from "@/components/Header.vue";
</script>

<template>
  <section class="container">
    <Header :seeAllLink="'/portfolio'" :seeAllText="'See All Project'">
      <template #title>Featured Projects</template>
    </Header>
    <div class="project-list">
      <FeaturedProjectItem />
    </div>
  </section>
</template>
