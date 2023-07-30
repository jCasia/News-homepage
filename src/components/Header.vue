<template>
  <header
    class="flex justify-between items-center px-3.5 py-6 fixed top-0 left-0 w-full h-[90px] bg-white"
  >
    <img :src="logo" alt="logo" className="w-1/6" />
    <Nav />
  </header>
</template>
<script>
import Nav from './Nav.vue';
import logo from '../assets/images/logo.svg';
export default {
  components: {
    Nav,
  },
  data() {
    return {
      logo: logo,
    };
  },
};
</script>
<style></style>
