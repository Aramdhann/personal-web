<script setup>
import { ref } from "vue";
import TechItem from "../components/TechItem.vue";
import VueWriter from "vue-writer";

const position = ref([
  "Fullstack Developer",
  "Frontend Developer",
  "UI/UX Designer",
]);
</script>

<template>
  <section class="container">
    <div class="hero">
      <div class="summary">
        <div class="name">
          <img src="../assets/images/verify.png" alt="verified name" />
          <div class="text">
            <p>Moch. Raditya Aulya Aramdhan</p>
            <span>as</span>
            <span id="position">
              <VueWriter
                :array="position"
                :typeSpeed="70"
                :eraseSpeed="70"
                :delay="800"
              />
            </span>
          </div>
        </div>
        <div class="description-summary">
          <span>Hey there! 👋</span> I'm a Telecommunication Engineering grad
          with almost 2 year of experience in building impactful websites. I
          thrive on creating user-friendly designs with a focus on
          functionality. Always staying up-to-date with the latest tech trends.
          Let's bring some of that web development passion to your projects!
          Check out my work and let's chat! 😊🚀
        </div>
        <TechItem />
      </div>
      <div class="profile">
        <div class="status">
          <div class="circle-1">
            <div class="circle-2"></div>
          </div>
          <p>Open to work</p>
        </div>
        <img
          src="../assets/images/photo.png"
          alt="photo profile"
          class="photo"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  width: 100%;
  padding: 115px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 30px;
}

.summary {
  width: 75%;
}

.profile .photo {
  width: 200px;
  object-fit: contain;
}

.name {
  gap: 20px;
  display: flex;
  align-items: center;
  font-size: 25px;
  margin-bottom: 20px;
}

.name img {
  width: 25px;
}

.text > span {
  margin-left: 5px;
}

#position {
  width: fit-content;
  color: var(--main-color);
}

.is-typed span.cursor {
  display: inline-block;
  width: 3px;
  background-color: var(--secondary-color);
  animation: blink 1s infinite;
}

.name .text p {
  font-weight: bold;
  background: linear-gradient(90deg, #fd4400 0%, #f2c94c 57.54%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  display: inline;
}

.description-summary {
  width: 80%;
}

.description-summary span {
  display: block;
  margin-bottom: 20px;
}

.status {
  display: flex;
  align-items: center;
  gap: 10px;
  color: var(--main-color);
  background: var(--white);
  padding: 3px 8px;
  border-radius: 8px;
  border: 2px solid var(--main-color);
  width: fit-content;
  transform: translate(-45px, 200px);
  cursor: default;
}

.status > p {
  font-size: 14px;
  font-weight: bolder;
}

.status-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: fit-content;
  animation: blink 1s linear infinite;
}

@media (max-width: 876px) {
  .hero {
    padding: 80px 0;
    display: flex;
    justify-content: center;
  }

  .summary {
    width: 100%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .name {
    font-size: 20px;
  }

  .name .text .position {
    display: block;
  }

  .description-summary {
    width: 100%;
  }
}
</style>
