<script setup>
import { computed } from "vue";
import { useRoute } from "vue-router";
import projects from "@/data/project-data.json";

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
    <h2>{{ project.data.title ?? "loading..." }}</h2>
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
  height: 300px;
  width: 500px;
  object-fit: cover;
  border-radius: 10px;
}

@media (max-width: 715px) {
  h2 {
    font-size: 16px;
  }
}

.header {
  margin: 30px 0;
  display: flex;
  align-items: center;
}

h2 {
  text-align: center;
  margin-bottom: 30px;
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
