<script setup>
import { ref } from 'vue';

const items = ref([
  {
    id: 1,
    name: "Github",
    link: "https://github.com/Aramdhann",
    icon: "bi bi-github",
  },
  {
    id: 2,
    name: "Gitlab",
    link: "https://gitlab.com/Aramdhann",
    icon: "bi bi-gitlab",
  },
  {
    id: 3,
    name: "LinkedIn",
    link: "https://www.linkedin.com/in/mochraditya",
    icon: "bi bi-linkedin",
  },
  {
    id: 4,
    name: "Discord",
    link: "https://discord.com/users/455921717513289750",
    icon: "bi bi-discord",
  },
]);
</script>

<template>
  <div class="footer">
    <div class="container">
      <div class="circle-1"><div class="circle-2"></div></div>
      <p>Let's connect:</p>
      <div v-for="(item, index) in items" :key="index" class="footer-icon">
        <a :href="item.link" target="_blank" class="tooltip">
          <i :class="item.icon"></i>
          <span class="tooltip-text">{{ item.name }}</span>
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
@media (max-width: 715px) {
  .container {
    display: flex;
    justify-content: center;
  }
}

p {
  font-size: 14px;
}

.footer {
  position: fixed;
  bottom: 0;
  display: flex;
  min-width: 100%;
  padding: 8px 0;
  background: var(--main-color);
}

.footer .container {
  display: flex;
  align-items: center;
  gap: 15px;
}

.footer-icon {
  display: flex;
  gap: 15px;
}

.footer-icon i {
  font-size: 24px;
  color: white;
  transition: 0.2s ease-out;
}

.footer-icon a {
  text-decoration: none;
}

.footer-icon i:hover {
  opacity: 0.7;
}
</style>
