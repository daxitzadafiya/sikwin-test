<template>
  <div>
    <b-container fluid="md">
      <b-row>
        <div class="col-2 pe-0 pe-sm-3">
          <div v-for="menu in menuList" :key="menu.id">
            <Menu-list :menuImg="menu.menuImg" />
          </div>
        </div>
        <div class="col-10 ">
          <div v-for="game in playGames" :key="game.id">
            <Game-section :playgameImg="game.playGameImg" :backgroundColor="game.backgroundColor" :filter="game.filter"/>
          </div>
        </div>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import GameSection from "./common/GameSection.vue";
import MenuList from "./common/MenuList.vue";
export default {
  components: { MenuList, GameSection },
  name: "game-types",
  data() {
    return {
      menuList: [
        {
          id: 1,
          menuImg: "used-active",
        },
        {
          id: 2,
          menuImg: "live",
        },
        {
          id: 3,
          menuImg: "sport",
        },
        {
          id: 4,
          menuImg: "lottery",
        },
        {
          id: 5,
          menuImg: "pocker",
        },
        {
          id: 6,
          menuImg: "game",
        },
      ],
      playGames: [
        {
          id: 1,
         playGameImg:"playgame-1",
        //  filter:"drop-shadow(1.414px 1.414px 1px rgba(0,0,0,0.3))",
        //  backgroundColor:"#0f0f0f"
        },
        {
          id: 2,
          playGameImg: "playgame-2",
        },
        {
          id: 3,
          playGameImg: "playgame-3",
        },
        {
          id: 4,
          playGameImg: "playgame-1",
        }
      ],
    };
  },
};
</script>

<style>
</style>