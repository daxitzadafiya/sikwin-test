<template>
  <div>
    <b-container fluid="md">
        <b-row>
            <Hot-game-box/>
        </b-row>
    </b-container>
  </div>
</template>

<script>
import HotGameBox from './common/HotGameBox.vue'
export default {
  components: { HotGameBox },
    name:'hot-game',
}
</script>

<style>

</style>