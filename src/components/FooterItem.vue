<script setup></script>

<template>
  <div class="footer">
    <div class="container">
      <p>Let's connect:</p>
      <div class="footer-icon">
        <a href="">
          <i class="bi bi-github"></i>
        </a>
        <a href="">
          <i class="bi bi-gitlab"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<style>
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
  font-size: 44px;
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
