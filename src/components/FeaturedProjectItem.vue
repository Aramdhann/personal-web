<template>
  <section class="container">
    <h1>Featured Project</h1>
    <div class="project-list">
      <div class="card-base-animate">
        <div class="card card-animate">
          <div class="card-banner"></div>
          <div class="card-content">
            <p class="card-title">title</p>
            <p>
              Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eveniet
              ipsa sunt deserunt et praesentium nam. Qui, veritatis aut?
              Adipisci deserunt porro minus delectus ea architecto iure minima
              sed, esse magni?
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
              <div class="card-tag"><p>tag caption</p></div>
              <div class="card-tag"><p>tag caption</p></div>
              <div class="card-tag"><p>tag caption</p></div>
              <div class="card-tag"><p>tag caption</p></div>
              <div class="card-tag"><p>tag caption</p></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.project-list {
  display: flex;
  padding: 10px 0;
  gap: 10px;
  overflow-y: auto;
}

.card-btn-list {
  display: flex;
  gap: 10px;
}

.card-btn-list > a {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 8px;
  border: none;
  border-radius: 7px;
  color: var(--white);
  transition: 0.4s;
  opacity: 1;
}

.card-btn-list a:hover {
  opacity: 0.7;
}

.card-btn-list a img {
  max-width: 30px;
  object-fit: contain;
}

.card-tag {
  font-size: 12px;
  display: flex;
  padding: 2px 5px 4px 5px;
  border-radius: 5px;
  width: fit-content;
  opacity: 1;
  transition: 0.4s;
  background: var(--blue); 
}

.card-tag:hover {
  opacity: 0.7;
  cursor: default;
}

.card-tag-list {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
}

/* width */
::-webkit-scrollbar {
  height: 6px;
  width: 6px;
}

/* Track */
::-webkit-scrollbar-track {
  background: var(--secondary-color);
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: var(--main-color);
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #af2f00;
}
</style>
