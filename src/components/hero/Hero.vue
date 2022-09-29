<script setup>
import axios from 'axios'
import { ref, onMounted } from 'vue'

const aboImg = ref([])
const staffImg = ref([])
const menuImg = ref([])
const galImg = ref([])
const newsImg = ref([])

const imgUrl = ref([])

onMounted(() => {
  axios.get('https://gastropub.webexam-mcdm.dk/api/images').then((res) => {
    aboImg.value = res.data && res.data[0] ? res.data[0] : 'none'
    staffImg.value = res.data && res.data[3].url ? res.data[3] : 'none'
    menuImg.value = res.data && res.data[9].url ? res.data[9] : 'none'
    galImg.value = res.data && res.data[13].url ? res.data[13] : 'none'
    newsImg.value = res.data && res.data[1].url ? res.data[1] : 'none'
  })
})

</script>
<!-- :style="{'background-image': `url(${aboImg.url})`}" -->
<template>
    <section class="w-full h-80 relative bg-cover bg-no-repeat bg-center flex justify-center items-center" :style="{'background-image': `url(${aboImg.url})`}">
        <div class="w-full h-full absolute top-0 left-0 bg-black opacity-60"></div>
        <h1 class="text-[86px] text-white z-10"></h1>
    </section>
</template>

<style>
</style>
