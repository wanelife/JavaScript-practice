<template>
  <div id="app">
    <router-view/>
    <footerGuide></footerGuide>
  </div>
</template>

<script>
import FooterGuide from './components/FooterGuide/FooterGuide.vue'
export default {
  components:{
    FooterGuide

  }
}
</script>

<style>
#app {
  width: 100%;
  height: 100%;
  background-color: #f5f5f5;
}
</style>
