<template>
  <div
    class="flex flex-col gap-5 mt-[90px] tabletsm:grid tabletsm:grid-cols-2 tabletsm:grid-rows-auto tabletsm:gap-8 laptop:mt-0 laptop:mb-8"
  >
    <img
      :src="heroImgMobile"
      alt="heroImg"
      class="w-full self-center tabletsm:hidden"
    />
    <img
      :src="heroImgDesk"
      alt="heroImg"
      class="w-full self-center hidden tabletsm:inline tabletsm:col-span-full"
    />
    <h1
      class="text-[2.5rem] leading-10 text-veryDarkBlue font-extrabold pr-5 tabletsm:self-center tabletsm:text-5xl laptoplg:text-[3.5rem]"
    >
      The Bright Future of Web 3.0?
    </h1>
    <div class="flex flex-col gap-5 tabletsm:self-center">
      <p class="text-darkGrayBlue">
        We dive into the next evolution of the web that claims to put the power
        of the platforms back into the hands of the people. But is it really
        fulfilling its promise?
      </p>
      <base-button label="Read More" />
    </div>
  </div>
</template>

<script>
import heroImgMobile from '../assets/images/image-web-3-mobile.jpg';
import heroImgDesk from '../assets/images/image-web-3-desktop.jpg';
export default {
  data() {
    return {
      heroImgMobile: heroImgMobile,
      heroImgDesk: heroImgDesk,
    };
  },
};
</script>
