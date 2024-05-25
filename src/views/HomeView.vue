<template>
  <div class="home">
    <div class="head">
      <h1>This is homepage</h1>
      <button @click="clickButton" class="button">{{buttonName}}</button>
    </div>
    <div v-if="showPage"><About></About></div>
  </div>
</template>

<script>
import { computed, ref } from 'vue'


import About from '../components/About'
export default {
  components: { About },
  setup(){
    let isActive =ref(false);
    let showPage=ref(false)
    let clickButton=()=>{
      showPage.value =! showPage.value;
      isActive.value =! isActive.value;
    }
    const buttonName = computed(()=>(
      isActive.value ? "Close" :"About Us"
    ))
    return {clickButton,showPage,buttonName}
  }
}
</script>
<style>
.head{
  display:flex;
  justify-content: space-between;
  margin: 0 auto;
  align-items: center;
  max-width: 1200px;
}
.button{
  background-color: rgb(10, 107, 97);
  color: white;
  font-weight: bold;
  border: 1px solid black;
  border-radius: 15px;
  padding: 10px;
  margin: 0;
  font-size: 15px;
  border:none;
}
</style>
