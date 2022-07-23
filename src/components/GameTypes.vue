<template>
  <div>
    <b-container fluid="md">
      <b-row>
        <div>
          <b-card no-body>
            <b-tabs pills card vertical>
              <b-tab
                v-for="menu in menuList"
                :key="menu.id"
                title="Tab 1"
                active
                @click="handleActiveTab(menu.id)"
              >
                <template #title>
                  <Menu-list :menuImg="menu.menuImg" />
                </template>
                <b-card-text v-for="game in playGames" :key="game.id"
                  ><Game-section :playgameImg="game.playGameImg" /></b-card-text
              ></b-tab>
            </b-tabs>
          </b-card>
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
          defaultName: "used",
        },
        {
          id: 2,
          menuImg: "live",
          defaultName: "live",
        },
        {
          id: 3,
          menuImg: "sport",
          defaultName: "sport",
        },
        {
          id: 4,
          menuImg: "lottery",
          defaultName: "lottery",
        },
        {
          id: 5,
          menuImg: "pocker",
          defaultName: "pocker",
        },
        {
          id: 6,
          menuImg: "game",
          defaultName: "game",
        },
      ],
      playGames: [
        {
          id: 1,
          playGameImg: "playgame-1",
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
        },
      ],
    };
  },
  methods: {
    handleActiveTab(id) {
      for (let i = 0; i < this.menuList.length; i++) {
        if (this.menuList[i].id == id) {
          this.menuList[i].menuImg = this.menuList[i].menuImg + "-active";
        } else {
          this.menuList[i].menuImg = this.menuList[i].defaultName;
        }
      }
    },
  },
};
</script>

<style scoped>
.card {
  background-color: transparent !important;
}
::v-deep .card-header {
  padding: 0 !important;
  max-width: 100px !important;
}
::v-deep .nav-link {
  padding: 0 !important;
}
::v-deep .card-body {
  padding: 0 !important;
}
::v-deep .nav-pills .nav-link.active,
.nav-pills .show > .nav-link {
  background-color: transparent;
}

@media (max-width: 600px) {
  ::v-deep .card-header {
    padding: 0 !important;
    max-width: 70px !important;
  }
}
@media (max-width: 450px) {
  ::v-deep .card-header {
    padding: 0 !important;
    max-width: 50px !important;
  }
}
@media (max-width: 350px) {
  ::v-deep .card-header {
    padding: 0 !important;
    max-width: 40px !important;
  }
}
@media (max-width: 250px) {
  ::v-deep .card-header {
    padding: 0 !important;
    max-width: 50px !important;
  }
}
</style>