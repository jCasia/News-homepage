<template>
  <Header />
  <main class="flex flex-col px-3.5 gap-12">
    <Hero />
    <NewNews />
    <News />
  </main>
</template>

<script>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import NewNews from './components/NewNews.vue';
import News from './components/News.vue';

export default {
  components: {
    Header,
    Hero,
    NewNews,
    News,
  },
};
</script>
