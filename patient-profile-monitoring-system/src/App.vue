<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/Login">Login</router-link>
    </div>
    <transition name="fade" mode="out-in">
      <router-view />
    </transition>
  </div>
</template>

<script>



export default {
  name:"App",
  components:{
    
  }
}
</script>

<style lang="scss">
@import '@/assets/styles/main.scss';



</style>
