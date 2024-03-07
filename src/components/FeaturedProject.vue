<script setup>
import FeaturedProjectItem from "@/components/FeaturedProjectItem.vue";
import Header from '@/components/Header.vue'
</script>

<template>
  <section class="container">
    <Header>
      <template #title>
        Featured Projects
      </template>
    </Header>
    <div class="project-list">
      <FeaturedProjectItem/>
      <FeaturedProjectItem/>
      <FeaturedProjectItem/>
      <FeaturedProjectItem/>
    </div>
  </section>
</template>

<style scoped>
.project-list {
  display: flex;
  padding: 10px 0;
  gap: 10px;
  overflow-x: auto;
}
</style>
