<script setup>
import CertificateItem from "@/components/CertificateItem.vue";
import Header from "@/components/Header.vue";
</script>

<template>
  <section class="container certificate">
    <Header
      :see-all-link="'/certificate'"
      :see-all-text="'See All Certificate'"
    >
      <template #title> Certificate & Competition </template>
    </Header>
    <div class="certif-list">
      <CertificateItem />
      <CertificateItem />
      <CertificateItem />
      <CertificateItem />
    </div>
  </section>
</template>

<style scoped>
.certif-list {
  display: flex;
  padding: 15px 0;
  gap: 10px;
  overflow-x: auto;
}

.certificate {
  padding: 115px 0px;
}
</style>
