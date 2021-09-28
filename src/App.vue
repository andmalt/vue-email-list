<template>
  <div id="app">
    <Main/>
  </div>
</template>

<script>
import Main from './components/Main.vue'
import Axios from 'axios'

export default {
  name: 'App',
  components: {
    Main,
  },
  Mounted(){
    console.log(Axios);
  }
}
</script>

<style lang="scss">
#app {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
