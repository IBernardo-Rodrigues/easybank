<template>
  <hero/>
  <features/>
  <latest-articles/>
  <home-footer/>
</template>

<script>
import Hero from '../components/Hero.vue';
import Features from '../components/Features.vue';
import LatestArticles from '../components/LatestArticles.vue';
import HomeFooter from '../components/Footer.vue';

export default {
  components: {
    Hero,
    Features,
    LatestArticles,
    HomeFooter
  }
}
</script>

<style lang="scss" scoped>

</style>