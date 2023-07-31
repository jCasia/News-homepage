<template>
  <div class="bg-veryDarkBlue p-5 flex flex-col laptoplg:p-7 laptop:mb-8">
    <h2 class="text-softOrange font-bold text-3xl laptoplg:text-4xl">New</h2>
    <div class="flex flex-col">
      <NewNewsCard
        v-for="news in newNews"
        :key="news.id"
        :title="news.title"
        :text="news.text"
      />
    </div>
  </div>
</template>

<script>
import NewNewsCard from './NewNewsCard.vue';

export default {
  components: {
    NewNewsCard,
  },
  data() {
    return {
      newNews: [
        {
          id: 1,
          title: 'Hydrogen VS Electric Cars',
          text: 'Will hydrogen-fueled cars ever catch up to EVs?',
        },
        {
          id: 2,
          title: 'The Downsides of AI Artistry',
          text: 'What are the possible adverse effects of on-demand Ai image generation?',
        },
        {
          id: 3,
          title: 'Is VC Funding Drying Up?',
          text: 'Private funding by VC firms is down 50% YOY. We take a look at what that means.',
        },
      ],
    };
  },
};
</script>
