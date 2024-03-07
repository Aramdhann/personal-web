<script setup></script>

<template>
  <div class="footer">
    <div class="container">
      <div class="circle-1"><div class="circle-2"></div></div>
      <p>Let's connect:</p>
      <div class="footer-icon">
        <a href="https://github.com/Aramdhann" target="_blank">
          <i class="bi bi-github"></i>
        </a>
        <a href="https://gitlab.com/Aramdhann" target="_blank">
          <i class="bi bi-gitlab"></i>
        </a>
        <a href="https://www.linkedin.com/in/mochraditya" target="_blank">
          <i class="bi bi-linkedin"></i>
        </a>
        <a href="https://discord.com/users/455921717513289750" target="_blank">
          <i class="bi bi-discord"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.footer {
  display: flex;
  padding: 18px 0;
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
  font-size: 32px;
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
