<template>
  <div class="container center-object">
    <div class="not-found">
      <img src="@/assets/images/404.png" alt="404 page not found" />
      <p>Sorry, Page Not Found! 😓</p>
    </div>
  </div>
</template>

<style>
.not-found img {
  /* width: 250px; */
  max-width: 35ty%;
  height: auto;
  display: flex;
}

.not-found {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 40px;
}

.not-found p {
  font-size: 40px;
  font-weight: 600;
  display: block;
}
</style>
