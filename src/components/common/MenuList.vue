<template>
  <div class="mb-3 pointer">
    <img
      :src="require(`@/assets/images/gameTypes/menuImg/${menuImg}.png`)"
      alt=""
      srcset=""
      class="img-fluid"
    />
  </div>
</template>

<script>
export default {
  name: "menu-list",
  props: ['menuImg'],
};
</script>

<style>
</style>