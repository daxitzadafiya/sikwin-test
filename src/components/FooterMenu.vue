<template>
  <div class="bottom-menu text-center d-flex justify-content-around align-items-center">
    <div v-for="menu in footerMenu" :key="menu.id">
      <img
            :src="require(`@/assets/images/footerMenu/${menu.menu}.png`)"
            alt=""
            srcset=""
            class="img-fluid w-75 pointer"
          />
    </div>
  </div>
</template>

<script>
export default {
  name: "bottom-menu",
  data() {
    return {
        footerMenu:[
            {
                id:1,
                menu:"home-active",
            },
            {
                id:2,
                menu:"gift",
            },
            {
                id:3,
                menu:"cost",
            },
            {
                id:4,
                menu:"message",
            },
            {
                id:5,
                menu:"account",
            }
        ]
    };
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
</style>