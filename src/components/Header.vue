<template>
  <div class="header">
    <h1>
      <slot name="title"></slot>
    </h1>
    <a href="">See all</a>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 25px;
}

.header a {
  display: block;
  text-decoration: none;
  color: var(--main-color);

  &:hover {
    opacity: 0.7;
    transition: 0.2s ease-out;
    border-bottom: 1px solid var(--main-color);
  }
}
</style>
