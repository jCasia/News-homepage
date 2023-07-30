<template>
  <button
    class="text-offWhite bg-softRed self-start py-3 w-1/2 uppercase tracking-[0.175em] font-medium hover:bg-veryDarkBlue hover:text-white transition-colors duration-300"
  >
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: String,
  },
};
</script>
