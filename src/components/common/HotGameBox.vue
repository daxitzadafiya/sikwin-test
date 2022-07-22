<template>
  <div class="py-4">
    <h4 class="mb-3 mt-2">Hot Game</h4>
    <carousel
      :autoplay="false"
      :per-page="5"
      :scroll-per-page="true"
      :pagination-enabled="false"
      :navigation-enabled="false"
    >
      <slide v-for="game in gameBox" :key="game.id" class="d-flex game-box me-3">
        <img
          :src="require(`@/assets/images/hotGames/${game.gameImg}.png`)" 
          alt=""
          srcset=""
          class="img-fluid"
        />
      </slide>
    </carousel>
  </div>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";
export default {
  name:'hot-game-box',
  components: {
    Carousel,
    Slide,
  },
  data() {
    return{
      gameBox: [
        {
          id:1,
          gameImg:"gameimg-1"
        },
        {
          id:2,
          gameImg:"gameimg-2"
        },
        {
          id:3,
          gameImg:"gameimg-3"
        },
        {
          id:4,
          gameImg:"gameimg-4"
        },
        {
          id:5,
          gameImg:"gameimg-5"
        },
        {
          id:6,
          gameImg:"gameimg-1"
        },
        {
          id:7,
          gameImg:"gameimg-2"
        },
        {
          id:8,
          gameImg:"gameimg-3"
        },
        {
          id:9,
          gameImg:"gameimg-4"
        },
        {
          id:10,
          gameImg:"gameimg-5"
        },
      ],
    }
  }
};
</script>

<style scoped>
.game-box {
  max-width: 144px;
  max-height: 144px;
  border-radius: 12px;
  background-color: #303031;
  border: 1px solid #1a1a1a;
  overflow: hidden;
}
.game-box img{
   width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>