<template>
  <div
    class="text-white flex flex-col gap-2 border-solid border-b border-grayishBlue py-6 last:border-b-0 last:pb-0"
  >
    <h3 class="font-bold text-xl">{{ title }}</h3>
    <p class="text-grayishBlue text-[.9rem]">{{ text }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    text: String,
  },
};
</script>
