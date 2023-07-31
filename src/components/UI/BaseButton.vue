<template>
  <button
    class="text-offWhite text-sm font-bold bg-softRed self-start py-3 w-1/2 uppercase tracking-[0.175em] hover:bg-veryDarkBlue hover:text-white transition-colors duration-300 mobilemd:text-base laptop:text-sm laptop:py-4 laptop:tracking-[0.3em]"
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
