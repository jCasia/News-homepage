<template>
  <div
    class="fixed top-0 left-0 w-full h-screen bg-black/50 tabletsm:hidden"
    :class="[isOpen ? 'visible opacity-100' : 'invisible opacity-0']"
    @click="closeMenu"
  ></div>
  <div
    class="fixed top-0 right-0 w-8/12 h-screen bg-white flex flex-col p-5 items-end gap-24 transition-all duration-500 tabletsm:hidden"
    :class="animateMenu"
  >
    <button type="button" aria-label="close menu" @click="closeMenu">
      <img :src="closeImg" alt="close menu" />
    </button>
    <ul class="self-start flex-1 flex flex-col gap-5">
      <li
        v-for="(link, index) in links"
        :key="index"
        class="transition-all delay-400 duration-1000"
        :class="listAnimation"
      >
        <a href="#" class="text-lg" @click="closeMenu">{{ link }}</a>
      </li>
    </ul>
  </div>
</template>
<script>
import close from '../assets/images/icon-menu-close.svg';
export default {
  props: ['isOpen', 'links', 'closeMenu'],
  data() {
    return {
      closeImg: close,
    };
  },
  computed: {
    animateMenu() {
      return this.isOpen
        ? 'visible opacity-100 translate-x-0'
        : 'invisible opacity-0 translate-x-full';
    },
    backDrop() {
      return this.isOpen ? 'visible opacity-100 ' : 'invisible opacity-0';
    },
    listAnimation() {
      return this.isOpen
        ? 'visible opacity-100 translate-x-0'
        : 'invisible opacity-0 even:-translate-x-1/2 odd:translate-x-1/2';
    },
  },
};
</script>
