<template>
    <main class=" mb-j-ct mb-max-w flex-col plain-card mb-p-lr-10 ">
    <slot></slot>
    <h1 class="mg-bm-20">{{ heading }}</h1>
    <p class="details text-a">{{ details }}</p>
    </main>

</template>
<script setup>
import '../assets/Styles/styles.css'
defineProps(['imgScr','heading', 'details'])

</script>
