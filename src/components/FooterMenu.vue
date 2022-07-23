<template>
  <div
    class="
      bottom-menu
      text-center
      d-flex
      justify-content-around
      align-items-center
    "
  >
    <div v-for="menu in footerMenu" :key="menu.id">
      <img
        :src="require(`@/assets/images/footerMenu/${menu.menu}.png`)"
        alt=""
        srcset=""
        class="img-fluid pointer"
        @click="handleActiveTab(menu.id)"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "bottom-menu",
  data() {
    return {
      footerMenu: [
        {
          id: 1,
          menu: "home-active",
          defaultName: "home",
        },
        {
          id: 2,
          menu: "gift",
          defaultName: "gift",
        },
        {
          id: 3,
          menu: "cost",
          defaultName: "cost",
        },
        {
          id: 4,
          menu: "message",
          defaultName: "message",
        },
        {
          id: 5,
          menu: "account",
          defaultName: "account",
        },
      ],
    };
  },
  methods: {
    handleActiveTab(id) {
      for (let i = 0; i < this.footerMenu.length; i++) {
        if (this.footerMenu[i].id == id) {
          this.footerMenu[i].menu = this.footerMenu[i].menu + "-active";
        } else {
          this.footerMenu[i].menu = this.footerMenu[i].defaultName;
        }
      }
    },
  },
};
</script>

<style scoped>
.bottom-menu {
  width: 100%;
  height: 100px;
  border-radius: 12px 12px 0px 0px;
  background-color: #1a1a1a;
  position: sticky;
  bottom: 0;
  z-index: 99;
}
.bottom-menu img {
  width: 75%;
}
@media (max-width: 500px) {
  .bottom-menu img {
    width: 50%;
  }
}
</style>