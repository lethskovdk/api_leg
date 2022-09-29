<script setup>
  import { defineProps } from "vue";

  const props = defineProps({name: String, ingredients: String, price: String})
</script>

<template>
  <div class="grid grid-cols-2 grid-rows-2">
    <h3>{{name}}</h3>
    <div class="row-span-2">{{price}}</div>
    <p>{{ingredients}}</p>
  </div>
</template>
