<script setup>
import Tag from "@/components/Tag.vue";
</script>

<template>
  <div class="card-base-animate">
    <div class="card card-animate">
      <div class="card-banner"></div>
      <div class="card-content">
        <p class="card-title">title</p>
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eveniet ipsa
          sunt deserunt et praesentium nam. Qui, veritatis aut? Adipisci
          deserunt porro minus delectus ea architecto iure minima sed, esse
          magni?
          <a class="text-link">Read more</a>
        </p>
        <div class="card-btn-list">
          <a href="" style="background: var(--main-color)"
            ><img src="../assets/images/view.png" alt="view project"
          /></a>
          <a href="" style="background-color: var(--black)"
            ><img src="../assets/images/git.png" alt="github project"
          /></a>
        </div>
        <div class="card-tag-list">
          <Tag>
            <template #title> tag caption </template>
          </Tag>
        </div>
      </div>
    </div>
  </div>
</template>
