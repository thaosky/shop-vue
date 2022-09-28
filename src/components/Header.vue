<template>
  <header class="l-header" id="header">
    <nav class="nav bd-container">
      <a href="#" class="nav__logo">Christmas</a>
      <div class="nav__menu" id="nav-menu" v-bind:class="{'show-menu': isShow}">
        <ul class="nav__list">
          <li class="nav__item"><a href="#home" class="nav__link">Home</a></li>
          <li class="nav__item"><a href="#share" class="nav__link">Share</a></li>
          <li class="nav__item"><a href="#decoration" class="nav__link">Decoration</a></li>
          <li class="nav__item"><a href="#accessory" class="nav__link">Accessory</a></li>
        </ul>
      </div>

      <div class="nav__toggle" id="nav-toggle" @click="toggleMenu">
        <i class="bx bx-grid-alt"></i>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isShow: true,
    }
  },
  methods: {
    toggleMenu() {
      this.isShow = !this.isShow
    }
  }
}
</script>

<style scoped>
.l-header {
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: var(--z-fixed);
  background-color: var(--body-color);
}

.nav {
  height: var(--header-height);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

@media screen and (max-width: 768px) {
  .nav__menu {
    position: fixed;
    top: -100%;
    left: 0;
    right: 0;
    width: 90%;
    margin: 0 auto;
    padding: 2.5rem 0 0;
    background-color: var(--body-color);
    transition: 0.4s;
    box-shadow: 0 0 4px rgba(0, 0, 0, 0.1);
    border-radius: 2rem;
    z-index: var(--z-fixed);

    text-align: center;
  }

  .nav__item {
    margin-bottom: var(--mb-3);
  }

  .nav__link, .nav__logo, .nav__toggle {
    color: var(--title-color);
    font-weight: var(--font-semi-bold);
  }

  .nav__logo:hover {
    color: var(--first-color);
  }

  .nav__link {
    transition: 0.3s;
  }

  .nav__link:hover {
    color: var(--first-color);
  }

  .nav__toggle {
    font-size: 1.3rem;
    cursor: pointer;
  }

  .show-menu {
    transition: 0.5s;
    top: calc(var(--header-height) + 1rem);
  }
}
</style>