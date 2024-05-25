<template>
  <Navbar></Navbar>
  <router-view/>
</template>
<script>
import Navbar from "./components/Navbar.vue"
export default{
  components:{
    Navbar
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f8f9fa;
  max-width: 1200px;
}
</style>
