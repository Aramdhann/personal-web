<template>
  <div class="container center-object vh-100">
    <div class="under-dev">
      <img src="/images/under_construction.png" alt="under construction" />
      <p>Under development!</p>
    </div>
    <a class="btn-back" href="/">
      <span>Home</span>
    </a>
  </div>
</template>

<style scoped>
a span {
  width: 100%;
  text-align: center;
}

.btn-back {
  display: flex;
  gap: 10px;
  font-size: 16px;
  padding: 15px;
  width: auto;
  min-width: 100px;
  border-radius: 10px;
  color: var(--white);
  border: none;
  background: var(--main-color);
  position: relative;

  &::before {
    content: "<";
    position: absolute;
    left: 15px;
    opacity: 0;
  }

  &:hover {
    transition: all 0.5s;
    padding: 15px 15px 15px 25px;
    &::before {
      opacity: 1;
      transition: all 0.5s;
    }
  }
}

.under-dev img {
  /* width: 250px; */
  max-width: 35%;
  height: auto;
  display: flex;
}

.under-dev {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 40px;
}

.under-dev p {
  font-size: 40px;
  font-weight: 600;
  display: block;
}
</style>
