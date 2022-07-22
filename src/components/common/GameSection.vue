<template>
  <div class="play-games mb-3 pointer">
    <img
      :src="require(`@/assets/images/gameTypes/gameSection/${playgameImg}.png`)"
      alt=""
      srcset=""
      class="img-fluid"
    />
    <div class="overlay">
      <div class="rounded-pill round-btn px-3 py-sm-2">
        <p class="m-0 mx-0 mx-sm-3">Maintained</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "game-section",
  props:[
    'playgameImg',
    'filter',
    'backgroundColor'
  ]
};
</script>

<style scoped>
.play-games {
  max-width: 578px;
  max-height: 150px;
  border-radius: 12px;
  background-color: #8b8780;
  overflow: hidden;
    position: relative;
}
.play-games img {
  width: 100%;
  height: 100%;
  object-fit: none;
}
.overlay {
  position: absolute;
  bottom: 0;
  background: rgba(0, 0, 0, 0.6); /* Black see-through */
  width: 100%;
  height: 100%;
  transition: .5s ease;
  opacity:0;
  font-size: 20px;
  padding: 20px;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}
.round-btn{
  background-color: #0f0f0f;
}
.play-games:hover .overlay {
  opacity: 1;
}
@media (max-width: 600px) {
  .play-games {
  border-radius: 12px;
  background-color: transparent;
  overflow: hidden;
}
 .play-games img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 12px;
}
}
</style>