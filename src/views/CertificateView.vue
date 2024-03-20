<script setup>
import CertificateItem from '@/components/CertificateItem.vue'
import certif from "@/data/certif-data.json";
</script>

<template>
  <div class="container project-list">
    <CertificateItem :items="certif"/>
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
