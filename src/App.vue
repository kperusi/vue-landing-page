<script setup>
import LandingPage from './components/LandingPage.vue';
import NavBar from './components/NavBar.vue'
import { ref } from 'vue';
const toggle = ref(false)
const active = ref('')
const show = ref('')
const margin = ref('')



const setToggle =()=>{
   
  if(toggle.value===true){
    toggle.value = false
    active.value='active'
    show.value='open'
    margin.value= ''
  }
  else if (toggle.value===false){
    toggle.value = true
    active.value= ''
    show.value='close'
    margin.value='margin'
  }
   console.log(margin.value)
}

</script>





<template>


<section class="flex-col">
    <NavBar :toggle="toggle" :show="show" :active="active" @set-toggle="setToggle" />
<LandingPage :margin="margin"/>
</section>
    <!-- <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" /> -->

   
</template>

  