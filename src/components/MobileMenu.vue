<template>
  <div class="hidden fixed top-0 right-0 w-8/12 h-screen bg-white">
    <img :src="closeImg" />
    <!-- <ul>
      <li v-for="(link, index) in linksArray" :key="index">
        <a href="#">{{ link }}</a>
      </li>
    </ul> -->
    <h1>{{ links }}</h1>
  </div>
</template>
<script>
import close from '../assets/images/icon-menu-close.svg';
export default {
  props: ['isOpen', 'links'],
  data() {
    return {
      closeImg: close,
    };
  },
};
</script>
