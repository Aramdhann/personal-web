<script setup>
import FeaturedProjectItem from '@/components/FeaturedProjectItem.vue'
</script>

<template>
  <div class="container project-list">
    <FeaturedProjectItem/>
  </div>
</template>

<style scoped>
.container {
  margin-top: 50px;
  margin-bottom: 50px;
}

.project-list {
  flex-wrap: wrap;
}
</style>
