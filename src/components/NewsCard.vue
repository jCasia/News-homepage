<template>
  <div class="flex gap-5">
    <img :src="image" :alt="`${title} image`" class="w-3/12 laptop:w-[27.5%]" />
    <div class="flex flex-col gap-1">
      <h2 class="text-grayishBlue font-bold text-3xl">{{ newsNumber }}</h2>
      <a
        class="font-bold text-lg hover:text-softRed transition-colors duration-300"
        href="#"
        >{{ title }}</a
      >
      <p class="text-darkGrayBlue text-md">{{ text }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    newsNumber: String,
    title: String,
    image: String,
    text: String,
  },
};
</script>
