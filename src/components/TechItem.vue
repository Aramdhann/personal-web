<script setup>
import { ref } from "vue";

// const techStack = ref([
//   { id: 1, name: "ReactJS", image: "../assets/images/tech-stack/react.svg" },
//   { id: 2, name: "Laravel", image: "../assets/images/tech-stack/laravel.svg" },
//   { id: 3, name: "VueJS", image: "../assets/images/tech-stack/vue.svg" },
//   {
//     id: 4,
//     name: "Javascript",
//     image: "../assets/images/tech-stack/javascript.svg",
//   },
//   {
//     id: 5,
//     name: "Typescript",
//     image: "../assets/images/tech-stack/typescript.svg",
//   },
//   { id: 6, name: "PHP", image: "../assets/images/tech-stack/php.svg" },
//   { id: 7, name: "JQuery", image: "../assets/images/tech-stack/jquery.svg" },
//   { id: 8, name: "NodeJS", image: "../assets/images/tech-stack/nodejs.svg" },
//   { id: 9, name: "Vuetify", image: "../assets/images/tech-stack/vuetify.svg" },
//   {
//     id: 10,
//     name: "Tailwind CSS",
//     image: "../assets/images/tech-stack/tailwind.svg",
//   },
//   {
//     id: 11,
//     name: "Bootstrap",
//     image: "../assets/images/tech-stack/bootstrap.svg",
//   },
//   { id: 12, name: "MySQL", image: "../assets/images/tech-stack/mysql.svg" },
//   { id: 13, name: "MongoDB", image: "../assets/images/tech-stack/mongodb.svg" },
//   {
//     id: 14,
//     name: "PostgreSQL",
//     image: "../assets/images/tech-stack/postgresql.svg",
//   },
//   { id: 15, name: "HTML 5", image: "../assets/images/tech-stack/html5.svg" },
//   { id: 16, name: "CSS 3", image: "../assets/images/tech-stack/css3.svg" },
//   { id: 17, name: "Python", image: "../assets/images/tech-stack/python.svg" },
//   {
//     id: 18,
//     name: "Tensorflow",
//     image: "../assets/images/tech-stack/tensorflow.svg",
//   },
//   { id: 19, name: "Git", image: "../assets/images/tech-stack/git.svg" },
// ]);
</script>

<template>
  <div class="tech">
    <div class="row">
      <img src="../assets/images/tech-stack/react.svg" alt="react js" />
      <img src="../assets/images/tech-stack/laravel.svg" alt="laravel" />
      <img src="../assets/images/tech-stack/vue.svg" alt="vue" />
      <img src="../assets/images/tech-stack/javascript.svg" alt="javascript" />
      <img src="../assets/images/tech-stack/typescript.svg" alt="typescript" />
      <img src="../assets/images/tech-stack/php.svg" alt="php" />
      <img src="../assets/images/tech-stack/jquery.svg" alt="jquery" />
      <img src="../assets/images/tech-stack/nodejs.svg" alt="nodejs" />
      <img src="../assets/images/tech-stack/vuetify.svg" alt="vuetify" />
      <img src="../assets/images/tech-stack/tailwind.svg" alt="tailwindcss" />
      <img src="../assets/images/tech-stack/bootstrap.svg" alt="bootstrap" />
      <img src="../assets/images/tech-stack/mysql.svg" alt="mysql" />
      <img src="../assets/images/tech-stack/mongodb.svg" alt="mongodb" />
      <img src="../assets/images/tech-stack/postgresql.svg" alt="postgresql" />
      <img src="../assets/images/tech-stack/html5.svg" alt="html5" />
      <img src="../assets/images/tech-stack/python.svg" alt="python" />
      <img src="../assets/images/tech-stack/tensorflow.svg" alt="tensorflow" />
      <img src="../assets/images/tech-stack/git.svg" alt="git" />
      <div>
        <p style="font-size: 20px; font-weight: lighter">+</p>
        <p>
          keep learning & <br />
          still counting
        </p>
      </div>
    </div>
  </div>
  <!-- <div class="tech">
    <ul class="row">
      <li v-for="tech in getTechStack" :key="tech.id">
        <img :src="tech.image" :alt="tech.name" />
      </li>
    </ul>
  </div> -->
</template>

<style>
.tech {
  margin-top: 35px;
  width: 90%;
}

.tech .row {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  margin-bottom: 10px;
}

.tech img {
  max-width: 38px;
  object-fit: contain;
  opacity: 0.5;
  transition: 0.4s;
}

.tech img:hover {
  opacity: 1;
}

.row > div {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-left: 10px;
  font-size: 10px;
  cursor: default;
}

@media (max-width: 876px) {
  .row {
    justify-content: center;
  }
}
</style>
