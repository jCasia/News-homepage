<template>
  <div class="flex flex-col gap-5">
    <img :src="heroImg" alt="heroImg" class="w-full" />
    <h1 class="text-[2.5rem] leading-10 text-veryDarkBlue font-extrabold pr-5">
      The Bright Future of Web 3.0?
    </h1>
    <p class="text-darkGrayBlue">
      We dive into the next evolution of the web that claims to put the power of
      the platforms back into the hands of the people. But is it really
      fulfilling its promise?
    </p>
    <base-button label="Read More" />
  </div>
</template>

<script>
import heroImg from '../assets/images/image-web-3-mobile.jpg';

export default {
  data() {
    return {
      heroImg: heroImg,
    };
  },
};
</script>
