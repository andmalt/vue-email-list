<template>
  <div class="main-content">
    <h1>Email list:</h1>
    <ul>
      <li v-for="(element,index) in mail" :key="index"> {{ element }} </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Main',
  props:{
    mail:Array,
  }
}
</script>


<style scoped lang="scss">
.main-content{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 3rem;
  & h1{
    color: rgb(163, 0, 0);
    font-size: 2.5rem;
    margin-bottom: 0.6rem;
  }
  & ul{
    list-style: none;
    & li{
      font-size: 1.7rem;
      margin: 0.7rem 0;
    }
  }
}
</style>
