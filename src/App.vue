<script setup>
import NavbarItem from "@/components/NavbarItem.vue";
import FooterItem from "@/components/FooterItem.vue";
import FraudItem from "@/components/FraudItem.vue";
</script>

<template>
  <FraudItem />
  <NavbarItem />
  <router-view></router-view>
  <FooterItem />
</template>
