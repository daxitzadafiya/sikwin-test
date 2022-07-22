<template>
  <div class="hero-slides">
    <carousel
      :autoplay="true"
      :per-page="1"
      :scroll-per-page="true"
      :pagination-enabled="true"
      :navigation-enabled="false"
    >
      <slide v-for="slide in slides" :key="slide.id" class="d-flex slides-img">
        <img
          :src="require(`@/assets/images/heroSection/${slide.slideImg}.png`)" 
          alt=""
          srcset=""
        />
      </slide>
    </carousel>
  </div>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";
export default {
  name: "hero-section",
  components: {
    Carousel,
    Slide,
  },
//   props:[
//     'slides'
//   ]
data() {
    return{
      slides: [
        {
          id:1,
          slideImg:"slide1"
        },
        {
          id:2,
          slideImg:"slide1"
        },
        {
          id:3,
          slideImg:"slide1"
        },
        {
          id:4,
          slideImg:"slide1"
        },
      ],
    }
  }
};
</script>

<style scoped>
.hero-slides .slides-img img{
    width: 100%;
    height: 300px;
    object-fit: cover;
}
::v-deep .VueCarousel-pagination{
    width: 100%;
    text-align: center;
    margin-top: -60px;
    z-index: 9;
}
::v-deep .VueCarousel-dot{
  padding: 5px !important;
  margin: 0 !important;
  outline: none !important;
  /* background-color: rgb(243, 185, 54) !important; */
}
@media (max-width: 400px) {
  .hero-slides .slides-img img{
    width: 100%;
    height: 150px;
    object-fit: cover;
}
}
</style>