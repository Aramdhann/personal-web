<script setup>
import NavbarItem from "@/components/NavbarItem.vue";
import FooterItem from "@/components/FooterItem.vue";
import FraudItem from "@/components/FraudItem.vue";
</script>

<template>
  <FraudItem />
  <NavbarItem />
  <div class="margin">
    <router-view></router-view>
  </div>
  <FooterItem />
</template>

<style scoped>
.margin {
  margin-bottom: 70px;
}
</style>
