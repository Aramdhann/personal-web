<script setup>
import Tag from "@/components/Tag.vue";
import Toast from "@/components/Toast.vue";
import { ref, computed } from "vue";

const props = defineProps({
  items: {
    type: Array,
    required: true,
  },
  limit: {
    type: Number,
    default: null,
  },
});

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
    return props.items.slice(0, props.limit);
  } else {
    return props.items;
  }
});
</script>

<template>
  <Toast v-if="showToast" />
  <div
    v-if="limitedItems && limitedItems.length > 0"
    v-for="(project, index) in limitedItems"
    :key="index"
  >
    <div class="card-base-animate">
      <div class="card card-animate">
        <router-link :to="`/portofolio/${project.data.id}`">
          <div class="banner-group">
            <img
              class="card-banner"
              :src="
                project.data.image
                  ? `/images/projects/${project.data.image}`
                  : '/images/no-image.jpg'
              "
              :alt="project.data.title"
            />
            <p>{{ project.data.status }}</p>
          </div>
        </router-link>
        <div class="card-content">
          <div>
            <router-link :to="`/portofolio/${project.data.id}`">
              <p class="card-title">
                {{ truncateDescription(project.data.title, 6) }}
              </p>
            </router-link>
            <p class="description">
              {{ truncateDescription(project.data.description, 15) }}
            </p>
          </div>

          <div class="button-list">
            <div class="card-btn-list">
              <a
                :href="project.data.links.view"
                style="background: var(--main-color)"
                @click="triggerToast"
                ><img src="/images/view.png" alt="view project"
              /></a>
              <a
                :href="project.data.links.github"
                style="background-color: var(--black)"
                ><img src="/images/git.png" alt="github project"
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
    </div>
  </div>
  <div v-else>No project data available</div>
</template>

<style scoped>
.banner-group {
  position: relative;
}

.banner-group p {
  position: absolute;
  top: 0;
  border-radius: 10px 0 0 0;
  padding: 5px;
  color: var(--white);
  background: var(--main-color);
}

.button-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.description {
  height: 70px;
}

.card-title:hover {
  text-decoration: underline;
}
</style>
