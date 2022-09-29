<script>
import { RouterLink } from 'vue-router'
import Modal from './Modal.vue'
import { defineProps } from 'vue'

export default {
  components: {
    Modal
  },
  data() {
    return {
      showModal: false
    }
  }
}
</script>

<template>
    <header class="h-24 mb-[-6rem] sticky top-0  z-50">
        <nav class="h-full flex items-center justify-between flex-wrap">
            <div class="container m-auto flex items-center justify-between">
                <div>

                </div>

                <div class="text-white">
                    <RouterLink class="mr-7" to="/">Home</RouterLink>
                    <RouterLink class="mr-7" to="/AboutUs">Om os</RouterLink>
                    <RouterLink class="mr-7" to="/OurTeam">Vores Team</RouterLink>
                    <RouterLink class="mr-7" to="/Menu">Menu</RouterLink>
                    <RouterLink class="mr-7" to="/Gallery">Gallery</RouterLink>
                    <RouterLink class="mr-7" to="/News">Nyheder</RouterLink>
                    <RouterLink class="mr-7" to="/Contact">Kontakt</RouterLink>
                    <button id="show-modal" class="bg-[#F1B356] hover:bg-[#a67c3c] text-black font-bold py-3 px-6 rounded-full" @click="showModal = true">Book bord</button>

                </div>
            </div>
        </nav>
    </header>

    <modal :show="showModal" @close="showModal = false"/>
</template>
