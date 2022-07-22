<template>
  <div id="app">
    <Header/>
    <router-view/>
    <Footer-menu/>
  </div>
</template>
<script>
import FooterMenu from './components/FooterMenu.vue';
import Header from './components/Header.vue';


export default {
  name: "Home",
  components: {
    Header,
    FooterMenu 
  },
};
</script>

<style>
#app{
  /* width: 750px; */
  /* margin: 0 auto; */
  background-color: #0f0f0f;
  color: #8b8780;
}
.dark-bg{
  background-color: #0f0f0f;
}
.text-gold{
  color: #efc275;
}
.pointer{
  cursor: pointer;
}
</style>
