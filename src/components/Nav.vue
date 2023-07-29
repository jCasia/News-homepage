<template>
  <nav>
    <!-- mobile -->
    <button
      type="button"
      aria-label="menu"
      className="tabletsm:hidden"
      @click="openMenu"
    >
      <img :src="bars" alt="menu" />
    </button>
    <!-- desktop -->
    <ul className="hidden tabletsm:flex tabletsm:gap-5">
      <li v-for="(link, index) in links" :key="index">
        <a href="#">{{ link }}</a>
      </li>
    </ul>
    <MobileMenu :isOpen="isOpen" :links:="links" />
  </nav>
</template>

<script>
import MobileMenu from './MobileMenu.vue';
import bars from '../assets/images/icon-menu.svg';

export default {
  components: {
    MobileMenu,
  },

  data() {
    return {
      bars: bars,
      isOpen: false,
      isDisabled: false,
      links: ['Home', 'News', 'Popular', 'Trending', 'Categories'],
    };
  },

  methods: {
    openMenu() {
      this.isOpen = true;
    },
    closeMenu() {
      this.isOpen = false;
      this.isDisabled = true;
      setTimeout(() => {
        this.isDisabled = false;
      }, 900);
    },
  },
};
</script>
