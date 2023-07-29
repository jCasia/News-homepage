<template>
  <div class="flex flex-col gap-8 mb-14">
    <NewsCard
      v-for="news in newsInfo"
      :key="news.id"
      :newsNumber="news.newsNumber"
      :title="news.title"
      :text="news.text"
      :image="news.image"
    />
  </div>
</template>
<script>
import NewsCard from './NewsCard.vue';
import image1 from '../assets/images/image-retro-pcs.jpg';
import image2 from '../assets/images/image-top-laptops.jpg';
import image3 from '../assets/images/image-gaming-growth.jpg';

export default {
  components: {
    NewsCard,
  },
  data() {
    return {
      newsInfo: [
        {
          id: 1,
          image: image1,
          newsNumber: '01',
          title: 'Reviving Retro PCs',
          text: 'What happens when old PCs are given modern upgrades?',
        },
        {
          id: 2,
          image: image2,
          newsNumber: '02',
          title: 'Top 10 Laptops of 2022',
          text: 'Our best picks for various needs and budgets.',
        },
        {
          id: 3,
          image: image3,
          newsNumber: '03',
          title: 'The Growth of Gaming',
          text: 'How the pandemic has sparked fresh oppurtunities',
        },
      ],
    };
  },
};
</script>
