<template>
  <div id="app">
    <Main/>
    <h1> {{ mailRandomic }} </h1>
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
  data:function(){
    return{
      mailRandomic:'',
    }
  },
  mounted(){

  Axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
  .then( res => {
    const result = res.data;
    this.mailRandomic = result.response;
    console.log(this.mailRandomic);
  });
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
