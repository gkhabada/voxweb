<template>
  <div id="app">
    <tour-items />
  </div>
</template>

<script>
import TourItems from './components/TourItems.vue'

export default {
  name: 'App',
  components: {
    TourItems
  }
}
</script>

<style lang="scss">
@import 'assets/fonts/font.css';

#app {
  font-family: "MuseoSansCyrl", Arial, sans-serif;
}

</style>
