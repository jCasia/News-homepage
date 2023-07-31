<template>
  <main
    class="laptop:w-full laptop:h-screen laptop:grid laptop:place-items-center"
  >
    <div
      class="flex flex-col px-3.5 w-full gap-12 mobilelg:px-8 tabletsm:max-w-[720px] mx-auto laptop:max-w-[1120px] laptop:grid laptop:grid-cols-[1fr_350px] laptop:grid-rows-auto laptop:py-10 laptop:gap-9 laptoplg:px-0"
    >
      <NavContainer />
      <Hero />
      <NewNews />
      <News />
    </div>
  </main>
</template>

<script>
import NavContainer from './components/NavContainer.vue';
import Hero from './components/Hero.vue';
import NewNews from './components/NewNews.vue';
import News from './components/News.vue';

export default {
  components: {
    NavContainer,
    Hero,
    NewNews,
    News,
  },
};
</script>
