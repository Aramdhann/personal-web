<script setup>
import { computed } from "vue";
import { useRoute } from "vue-router";
import projects from "@/data/project-data.json";
import Tag from "@/components/Tag.vue";

const route = useRoute();

const projectId = computed(() => parseInt(route.params.id));
const project = computed(() =>
  projects.find((item) => item.data.id === projectId.value)
);
</script>

<template>
  <div class="container">
    <div class="header">
      <a type="button" @click="$router.back()">Go Back</a>
    </div>
    <div class="title">
      <h2>{{ project.data.title ?? "loading..." }}</h2>
      <span>{{ project.data.status }}</span>
    </div>
    <div class="card-tag-list">
      <Tag v-for="(tag, index) in project.data.tags.type" :key="index">
        <template #title>{{ tag }}</template>
      </Tag>
    </div>
    <div class="image-group">
      <img
        class="image"
        :src="
          project.data.image
            ? `/images/projects/${project.data.image}`
            : '/images/no-image.jpg'
        "
        :alt="project.data.title"
      />
    </div>
    <p>{{ project.data.description }}</p>
  </div>
</template>

<style scoped>
.title {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
  gap: 10px;
}

.title span {
  padding: 2px 5px;
  border-radius: 5px;
  background: var(--main-color);
  margin-bottom: 10px;
}

.card-tag-list {
  display: flex;
  justify-content: center;
  margin-bottom: 30px;
}

p {
  width: 70%;
  margin: 0 auto;
}

.image-group {
  width: 100%;
  justify-content: center;
  display: flex;
  margin-bottom: 30px;
}

.image {
  width: 900px;
  max-width: 100%;
  height: auto;
  border-radius: 10px;
}

@media (max-width: 715px) {
  h2 {
    font-size: 16px;
  }
  .title span {
    font-size: 14px;
  }
}

@media (max-width: 1140px) {
  p {
    width: 95%;
  }
}

.header {
  margin: 30px 0;
  display: flex;
  align-items: center;
}

h2 {
  text-align: center;
  margin-bottom: 10px;
}

a {
  display: block;
  left: 0;
  text-decoration: none;
  color: var(--main-color);
  cursor: pointer;
  width: fit-content;

  &:hover {
    opacity: 0.7;
    transition: 0.2s ease-out;
    border-bottom: 1px solid var(--main-color);
  }
}
</style>
