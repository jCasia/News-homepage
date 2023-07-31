<template>
  <div
    class="flex justify-between items-center px-3.5 py-6 fixed top-0 left-0 w-full h-[90px] bg-white mobilelg:p-8 laptop:relative laptop:col-span-full laptop:h-auto laptop:p-0"
  >
    <img :src="logo" alt="logo" className="w-1/6  tabletsm:w-1/12" />
    <Nav />
  </div>
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
