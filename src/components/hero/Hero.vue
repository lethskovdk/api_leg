<script setup>
import { defineProps } from 'vue'

const props = defineProps({heading: String, imgUrl: String})

</script>
<!-- :style="{'background-image': `url(${aboImg.url})`}" -->
<template>
    <section class="w-full h-80 relative bg-cover bg-no-repeat bg-center flex justify-center items-center" :style="{'background-image': `url(${imgUrl})`}">
        <div class="w-full h-full absolute top-0 left-0 bg-black opacity-60"></div>
        <h1 class="text-[86px] text-white z-10">{{heading}}</h1>
    </section>
</template>

<style>
</style>
