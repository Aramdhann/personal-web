<script setup>
import FeaturedProjectItem from '@/components/FeaturedProjectItem.vue'
import projects from "@/data/project-data.json";
</script>

<template>
  <div class="container project-list">
    <FeaturedProjectItem :items="projects"/>
  </div>
</template>

<style scoped>
.container {
  margin-top: 50px;
  margin-bottom: 50px;
}

.project-list {
  flex-wrap: wrap;
  justify-content: center;
}
</style>
