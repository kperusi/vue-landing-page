<script setup>
import '../assets/Styles/styles.css'
import { defineProps} from 'vue';
import { defineEmits } from 'vue';
defineProps({'toggle':Boolean, 
'active':String,
'show':String})

defineEmits(["setToggle"]);


</script>


<template>
  <section class="flex-col max-w">
  
  <main role="NAV BAR WRAP" 
  class="nav-main mb-z space-bw p-lr-3 flex-rw p-tb-20 width-mx mb-max-w mb-p-t-b">
  <img src="../assets/logo.svg" alt="" width="130" height="30">
    <nav role="navbar container">
      <ul class = 'list-wrap no-list-style flex-rw gap-10 mb-no-display' role="navLink containers">
        <li class="h-max">Home</li>
        <li>About</li>
        <li>Contact</li>
        <li>Blog</li>
        <li>Careers</li>
      </ul>
    </nav>
    <button class="hover btn bdr-rx-10 mb-no-display">Request Invite</button>
    <div :class="{hambuger:'hambuger', active:active}" @click="$emit('setToggle')">
    <span></span>
    <span></span>
    <span></span>
    </div>
  
    <!-- <h1>{{show }}</h1> -->
  </main>

  <div :class = "[`menu ${show}`]">
    <ul :class = "[`mb-nav-list  ${show}`]" role="navLink containers">
        <li>Home</li>
        <li>About</li>
        <li>Contact</li>
        <li>Blog</li>
        <li>Careers</li>
      </ul>
  </div>
</section>
</template>
