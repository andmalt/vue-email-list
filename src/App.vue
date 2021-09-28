<template>
  <div id="Container">
    <Main :mail="emails" />
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
      emails:[],

    }
  },
  mounted(){

    for(let i = 0; i < 10 ; i++){
    Axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
      .then( res => {
      const result = res.data;
      this.mailRandomic = result.response;
      this.emails.push(this.mailRandomic);
      });

    }
    console.log(this.emails)
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
