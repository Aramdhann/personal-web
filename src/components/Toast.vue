<script setup>
const props = defineProps({
  action: String,
});

const message = `There is no content ${props.action}`;
</script>

<template>
  <div class="modal">
    {{ message }}
    <span class="close">&times;</span>
  </div>
</template>

<style scoped>
.modal {
  width: fit-content;
  position: sticky;
  top: 80px;
  margin-left: auto;
  z-index: 100;
  margin-top: 10px;
  margin-right: 10px;
  background: #ae2727;
  border: 2px solid #cf6f6f;
  border-radius: 8px;
  padding: 10px;
}

.close {
  margin-left: 10px;
}
</style>
