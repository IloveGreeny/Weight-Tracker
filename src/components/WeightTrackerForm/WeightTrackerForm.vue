<script setup>
import {ref} from "vue";

const weight = ref("60 kg");
const height = ref("174 cm");

</script>


<template>
<form class="border-amber-100 bg-amber-700">
<h1>Add Data</h1>
  <p>Enter your weight</p>
  <input type="text" placeholder="Enter your weight(kg)"/>
  <input type="text" placeholder="Enter your height(cm)"/>
  <button @click="console.log(1)">ADD</button>
  <div>
    <h1>Facts</h1>
    <div>
      <p>Current weight {{weight}}</p>
      <p>Current height {{height}}</p>
    </div>
  </div>
</form>
</template>



<style scoped>

</style>