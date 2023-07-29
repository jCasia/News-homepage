<template>
  <div class="flex gap-5">
    <img :src="image" :alt="`${title} image`" class="w-3/12" />
    <div class="flex flex-col gap-1">
      <h2 class="text-grayishBlue font-bold text-3xl">{{ newsNumber }}</h2>
      <h3 class="font-bold text-lg">{{ title }}</h3>
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
