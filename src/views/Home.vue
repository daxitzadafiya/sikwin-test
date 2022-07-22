<template>
  <div class="home">
    <Hero-section/>
    <Hot-game/>
    <Pocket/>
    <Game-types/>
  </div>
</template>

<script>
import GameTypes from '../components/GameTypes.vue';
import HeroSection from '../components/HeroSection.vue';
import HotGame from '../components/HotGame.vue';
import Pocket from '../components/Pocket.vue';


export default {
  name: "Home",
  components: {
    HeroSection,
    HotGame,
    Pocket,
    GameTypes,
  },
};
</script>
<style>
</style>
