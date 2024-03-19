<script setup>
import { ref } from "vue";

const techStacks = ref([
  { id: 1, name: "ReactJS", image: "react.svg" },
  { id: 2, name: "Laravel", image: "laravel.svg" },
  { id: 3, name: "VueJS", image: "vue.svg" },
  {
    id: 4,
    name: "Javascript",
    image: "javascript.svg",
  },
  {
    id: 5,
    name: "Typescript",
    image: "typescript.svg",
  },
  { id: 6, name: "PHP", image: "php.svg" },
  { id: 7, name: "JQuery", image: "jquery.svg" },
  { id: 8, name: "NodeJS", image: "nodejs.svg" },
  { id: 9, name: "Vuetify", image: "vuetify.svg" },
  {
    id: 10,
    name: "Tailwind CSS",
    image: "tailwind.svg",
  },
  {
    id: 11,
    name: "Bootstrap",
    image: "bootstrap.svg",
  },
  { id: 12, name: "MySQL", image: "mysql.svg" },
  { id: 13, name: "MongoDB", image: "mongodb.svg" },
  {
    id: 14,
    name: "PostgreSQL",
    image: "postgresql.svg",
  },
  { id: 15, name: "HTML 5", image: "html5.svg" },
  { id: 16, name: "CSS 3", image: "css3.svg" },
  { id: 17, name: "Python", image: "python.svg" },
  {
    id: 18,
    name: "Tensorflow",
    image: "tensorflow.svg",
  },
  { id: 19, name: "Git", image: "git.svg" },
]);
</script>

<template>
  <div class="tech">
    <div class="row">
      <div v-for="techStack in techStacks" :key="techStack.id" class="tooltip">
      <img :src="`./src/assets/images/tech-stack/${techStack.image}`" :alt="techStack.name" />
      <span class="tooltip-text">
        {{techStack.name}}
      </span>
    </div>
      <div>
        <p style="font-size: 20px; font-weight: lighter">+</p>
        <p>
          keep learning & <br />
          still counting
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.tooltip {
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted black;
}

.tooltip .tooltip-text {
  visibility: hidden;
  width: 120px;
  background-color: #555;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 5px 0;
  position: absolute;
  z-index: 1;
  bottom: 125%;
  left: 50%;
  margin-left: -60px;
  opacity: 0;
  transition: opacity 0.3s;
}

.tooltip .tooltip-text::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: #555 transparent transparent transparent;
}

.tooltip:hover .tooltip-text {
  visibility: visible;
  opacity: 1;
}

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
