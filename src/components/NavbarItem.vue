<template>
  <nav id="nav">
    <div class="container">
      <div class="nav-content">
        <div class="nav-item-group">
          <router-link class="nav-item" to="/"
            >😁<span>It's me</span></router-link
          >
          <router-link class="nav-item" to="/portofolio"
            >💼<span>Portofolio</span></router-link
          >
          <router-link class="nav-item" to="/certificate"
            >✅<span>Certified</span></router-link
          >
          <router-link class="nav-item" to="/blog"
            >📖<span>Blog</span></router-link
          >
        </div>
        <div class="btn-base-animate">
          <a class="btn-animate" href="mailto:radityamochamad@gmail.com"
            >🤝<span>Collaborate</span></a
          >
        </div>
      </div>
    </div>
  </nav>
</template>

<style scoped>
#nav {
  display: flex;
  align-items: center;
  background-color: var(--main-color);
  top: 0;
  position: sticky;
  z-index: 100;
  padding: 15px 0;
}

#nav a {
  display: flex;
  align-items: center;
  gap: 5px;
  border-radius: 8px;
}

.nav-content {
  display: flex;
  justify-content: space-between;
}

.nav-item-group {
  display: flex;
  gap: 10px;
}

#nav .nav-item-group .nav-item.router-link-active,
#nav .nav-item-group .nav-item:hover {
  background: var(--black);
  transition: 0.2s ease-out;
  border-radius: 8px;
}

.nav-item {
  display: flex;
  color: var(--white);
  padding: 10px;
}

.btn-base-animate:hover {
  transform: translate(2px, -2px);
}

.btn-animate:hover {
  transition: 0.1s;
  transform: translate(5px, -5px);
  box-shadow: -5px 5px var(--secondary-color);
}

.btn-animate {
  display: flex;
  color: var(--white);
  padding: 10px;
  background: var(--black);
  border-radius: 8px;
}

@media (max-width: 715px) {
  #nav {
    padding: 10px 0;
  }
  
  .nav-item span {
    display: none;
  }

  .btn-animate span {
    display: none;
  }

  .nav-item.router-link-active > span {
    display: block;
    transition: 0.4s ease-out;
  }

  .nav-content {
    display: flex;
    justify-content: center;
    gap: 10px;
  }
}

@media (max-width: 1140px) {
  .nav-item span {
    font-size: 12px;
  }
}
</style>
