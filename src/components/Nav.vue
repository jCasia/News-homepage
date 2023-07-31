<template>
  <nav>
    <!-- mobile -->
    <button
      type="button"
      aria-label="menu"
      className="tabletsm:hidden"
      @click="openMenu"
      :disabled="isDisabled"
    >
      <img :src="bars" alt="menu" />
    </button>
    <MobileMenu :isOpen="isOpen" :links="links" :closeMenu="closeMenu" />
    <!-- desktop -->
    <ul className="hidden tabletsm:flex tabletsm:gap-5 laptop:gap-10">
      <li v-for="(link, index) in links" :key="index">
        <a
          href="#"
          class="text-darkGrayBlue hover:text-softRed transition-colors duration-300"
          >{{ link }}</a
        >
      </li>
    </ul>
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
      links: ['Home', 'New', 'Popular', 'Trending', 'Categories'],
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
      }, 500);
    },
  },
};
</script>
