<template>
  <header class="flex justify-between items-center px-3.5 py-6">
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
