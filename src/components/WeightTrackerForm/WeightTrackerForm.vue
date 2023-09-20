<script setup>
import {ref} from "vue";


</script>


<template>
<form class="border-amber-100 bg-amber-700">
<h1>Add Data</h1>
  <p>Enter your weight</p>
  <input type="text" placeholder="Enter your weight(kg)"/>
  <input type="text" placeholder="Enter your height(cm)"/>
  <button @click="console.log(1)">ADD</button>
</form>
</template>



<style scoped>

</style>