<script setup lang="ts">
import MainBanner from './components/MainBanner.vue';
import MainHeader from './components/MainHeader.vue';
import NewsComponent from './components/NewsComponent.vue';
import TopTierComponent from './components/TopTierComponent.vue';

</script>

<template>
  <main>
    <MainHeader class="header" />
    <MainBanner class="banner" />
    <NewsComponent class="news" />
    <TopTierComponent class="top" />
  </main>
</template>

<style lang="scss" scoped>
@media screen and (min-width: 1024px) {
  main {
    display: grid;
    grid-template-areas: "header header header header" "banner banner banner news" "top top top top";
    column-gap: 2rem;
  }
  .header  {
    grid-area: header;
  }
  .banner  {
    grid-area: banner;
  }
  .news  {
    grid-area: news;
  }
  .top  {
    grid-area: top;
  }
}
</style>
