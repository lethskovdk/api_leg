<script setup>
import axios from 'axios'
import { ref, onMounted } from 'vue'

const FooterTxtAdr = ref('')
const FooterTxtTlf = ref('')
const FooterTxtOpen = ref('')

onMounted(() => {
  axios.get('https://gastropub.webexam-mcdm.dk/api/texts').then((res) => {
    FooterTxtAdr.value = res.data && res.data[9] ? res.data[9] : 'none'
    FooterTxtTlf.value = res.data && res.data[10] ? res.data[10] : 'none'
    FooterTxtOpen.value = res.data && res.data[11] ? res.data[11] : 'none'
  })
})
</script>

<template>
  <section class="bg-[#2E2925]">
    <div class="container mx-auto grid grid-cols-2 py-16">
      <div class="contactarea">
        <div class="w-2/3 text-white">
          <h3>Kære kunde</h3>
          <p>Du er altid velkommen til at kontakte os For spørgsmål angående Deklarations indhold, allegener, eller økologiske forhold. Andre spørgsmål til Gastropub er også velkomne her.</p>
        </div>
        <form action="/action_page.php">
          <input type="text" id="name" name="fname" value="Navn *"><br><br>
          <input type="text" id="phone" name="fname" value="Telefon *"><br><br>
          <input type="text" id="text" name="lname" value="Besked *"><br><br>
          <input type="submit" value="Submit">
        </form>
      </div>
      <div class="infoarea text-white">
        <div class="item">
          <h3>{{FooterTxtAdr.description}}</h3>
        </div>
        <div class="item">
          <h3>{{FooterTxtTlf.description}}</h3>
        </div>
        <div class="item">
          <h3>{{FooterTxtOpen.description}}</h3>
          <p>Frokost servering - 12:00 - 15:00</p>
        </div>
      </div>
    </div>
  </section>
</template>
