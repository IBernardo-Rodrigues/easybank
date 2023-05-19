<template>
  <header>
    <div class="logo-wrapper">
      <img :src="logoImg" alt="Logo"/>
    </div>

    <button class="menu-toggler" @click="menuToggler">
      <img :src="menuTogglerIcon" alt="Menu"/>
    </button>
    <nav :class="{'opened': menuIsOpened}">
      <ul class="menu">
        <li class="menu-item">
          <router-link to="/" class="menu-link">Home</router-link>
        </li>
        <li class="menu-item">
          <router-link to="/" class="menu-link">About</router-link>
        </li>
        <li class="menu-item">
          <router-link to="/" class="menu-link">Contact</router-link>
        </li>
        <li class="menu-item">
          <router-link to="/" class="menu-link">Blog</router-link>
        </li>
        <li class="menu-item">
          <router-link to="/" class="menu-link">Careers</router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import logoImg from '../assets/img/logo.svg';
import menuOpenIcon from '../assets/img/icon-hamburger.svg';
import menuCloseIcon from '../assets/img/icon-close.svg';

export default {
  data() {
    return {
      logoImg,
      menuIsOpened: false, 
    }
  },
  methods: {
    menuToggler() {
      this.menuIsOpened = !this.menuIsOpened;
    }
  },
  computed: {
    menuTogglerIcon() {
      if (this.menuIsOpened) {
        return menuCloseIcon;
      }

      return menuOpenIcon;
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/mixins';

  header {
    position: sticky;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 80px;
    background-color: #fff;
    z-index: 3;
    padding: 0 .8rem;

    @include desktop {
      padding: 0 8rem;
    }
  }

  .menu-toggler {
    border: none;
    background: transparent;

    @include desktop {
      display: none;
    }
  }

  nav {
    position: absolute;
    top: 80px;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(#2d314d, transparent 65%);
    opacity: 1;
    transition: .3s;
    z-index: 3;

    &.opened {
      left: 0;
      right: 0;
      opacity: 1;

      .menu {
        left: 0;
      }
    }

    @include desktop {
      position: static;
      display: block;
      opacity: 1;
      background: transparent;
    }
  }

  .menu {
    position: relative;
    left: -10000px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    list-style: none;
    background-color: #fff;
    width: 90%;
    margin: 1.5rem auto;
    padding: 2rem;
    border-radius: .3rem;
    transition: .4s;

    @include desktop {
      position: static;
      flex-direction: row;
      justify-content: space-between;
      background-color: transparent;
      margin: 0;
      padding: 0;
      width: 100%;
    }
  }
  
  .menu-item {
    margin-bottom: 1rem;

    @include desktop {
      margin: 0;
    }
  }

  .menu-link {
    text-decoration: none;
    font-size: 18px;
    color: #2d314d;
  }

</style>