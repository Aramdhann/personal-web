<script setup>
const props = defineProps({
  seeAllLink: { type: String, default: "#" },
  seeAllText: { type: String, default: "See All" },
});
</script>

<template>
  <div class="header">
    <h1>
      <slot name="title"></slot>
    </h1>
    <router-link :to="seeAllLink">{{ seeAllText }}</router-link>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 25px;
}

a {
  display: block;
  text-decoration: none;
  color: var(--main-color);
  cursor: pointer;
  text-align: right;

  &:hover {
    opacity: 0.7;
    transition: 0.2s ease-out;
    border-bottom: 1px solid var(--main-color);
  }
}
</style>
