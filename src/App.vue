<template>
  <Header />
  <main>
    <Hero />
    <News />
    <NewNews />
  </main>
</template>

<script>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import News from './components/News.vue';
import NewNews from './components/NewNews.vue';

export default {
  components: {
    Header,
    Hero,
    NewNews,
    News,
  },
};
</script>
