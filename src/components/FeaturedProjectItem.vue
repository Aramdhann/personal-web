<script setup>
import Tag from "@/components/Tag.vue";
import Toast from "@/components/Toast.vue";
import { ref, computed } from "vue";

const props = defineProps({
  items: {
    type: Array,
    required: true
  },
  limit: {
    type: Number,
    default: null
  }
})

const showToast = ref(false);

const triggerToast = () => {
  showToast.value = true;
  setTimeout(() => {
    showToast.value = false;
  }, 3000);
};

const truncateDescription = (description, limit) => {
  const words = description.split(" ");
  if (words.length > limit) {
    return words.slice(0, limit).join(" ") + " ...";
  }
  return description;
};

const limitedItems = computed(() => {
  if (props.limit !== null) {
    return props.items.slice(0, props.limit)
  } else {
    return props.items
  }
})
</script>

<template>
  <Toast v-if="showToast" />
  <a
    v-if="limitedItems && limitedItems.length > 0"
    v-for="(project, index) in limitedItems"
    :key="index"
    :href="`/portofolio/${project.data.project_id}`"
  >
    <div class="card-base-animate">
      <div class="card card-animate">
        <img
          class="card-banner"
          :src="`./src/assets/images/projects/${project.data.image}`"
          :alt="project.data.title"
        />
        <div class="card-content">
          <p class="card-title">{{ project.data.title }}</p>
          <p class="description">
            {{ truncateDescription(project.data.description, 20) }}
          </p>
          <div class="card-btn-list">
            <a
              type="button"
              :href="project.data.links.view"
              style="background: var(--main-color)"
              @click="triggerToast"
              ><img src="../assets/images/view.png" alt="view project"
            /></a>
            <a
              :href="project.data.links.github"
              style="background-color: var(--black)"
              ><img src="../assets/images/git.png" alt="github project"
            /></a>
          </div>
          <div class="card-tag-list">
            <Tag v-for="(tag, index) in project.data.tags.type" :key="index">
              <template #title>{{ tag }}</template>
            </Tag>
          </div>
        </div>
      </div>
    </div>
  </a>
  <div v-else>No project data available</div>
</template>

<style scoped>
.description {
  height: 70px;
}
</style>