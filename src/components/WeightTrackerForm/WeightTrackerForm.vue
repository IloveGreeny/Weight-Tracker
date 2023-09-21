<script setup>
import {ref} from "vue";

let weight = ref("");
let height = ref("");



function addWeight() {
  event.preventDefault();
  let val = document.getElementById("weight").value;
  weight.value = val
  console.log(weight);
  let val2 = document.getElementById("height").value;
  height.value= val2;
  console.log(height);
}


</script>


<template>
<form class="border-amber-100 bg-amber-700">
<h1>Add Data</h1>
  <p>Enter your weight</p>
  <input type="text" id="weight" placeholder="Enter your weight(kg)"/>
  <input type="text" id="height" placeholder="Enter your height(cm)"/>
  <button  @click="addWeight()">ADD</button>
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