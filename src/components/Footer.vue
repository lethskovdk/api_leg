<script setup>
import { ref, onMounted } from 'vue'

const texts = ref(window.txt)
</script>

<template>
    <footer class="flex py-24 bg-[#211E1B]">
        <div class="container mx-auto">
            <div class="flex flex-row justify-between">
                <div class="w-72">
                    <h3 class="text-[25px] text-white">Information</h3>
                    <p class="text-white">En gastropub er en hybrid pub, bar og restaurant, der er kendt for servering af alkoholiske drikkevarer og mad.</p>
                </div>
                <div class="w-72">
                    <h3 class="text-[25px] text-white">Kontakt</h3>
                    <p class="text-white">{{texts[9].description}}</p>
                    <p class="text-white">{{texts[10].description}}</p>
                </div>
                <div class="w-72">
                    <h3 class="text-[25px] text-white">Social Media</h3>
                    <div class="flex justify-between">
                        <i></i>
                        <i></i>
                        <i></i>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
