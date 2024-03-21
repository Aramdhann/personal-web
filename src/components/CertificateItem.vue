<script setup>
import { computed } from "vue";

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
  <div
    v-if="limitedItems && limitedItems.length > 0"
    v-for="(certif, index) in limitedItems"
    :key="index"
    class="card-base-animate"
  >
    <div class="card-certif card-animate">
      <div class="card-content">
        <div class="card-header">
          <img :src="`/images/${certif.data.type}.png`" alt="icon" />
          <div>
            <p class="certif-title">{{ certif.data.title }}</p>
            <p>held by {{ certif.data.by }}</p>
          </div>
        </div>
        <p class="description">
          {{ truncateDescription(certif.data.description, 15) }}
        </p>
        <div class="card-tag-list">
          <div class="card-tag">
            Certified at {{ certif.data.certified_date }}
          </div>
          <div v-if="certif.data.due_to" class="card-tag">
            Due to {{ certif.data.due_to }}
          </div>
        </div>
      </div>
    </div>
  </div>
  <div v-else>No certificate data available</div>
</template>

<style scoped>
.card-content {
  gap: 15px;
}

@media (max-width: 876px) {
  .certificate {
    padding: 80px 0;
  }
}
</style>
