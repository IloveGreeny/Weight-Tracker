<script setup>
import {ref} from "vue";

let weight = ref("");
let height = ref("");
let bmi = ref(0);
let weightList = [];



function addWeight() {
  event.preventDefault();
  let val = document.getElementById("weight").value;
  weight.value = val;
  weightList.push(weight.value);
  let val2 = document.getElementById("height").value;
  height.value= val2;
}

function calculate() {
  event.preventDefault();

  console.log(weight.value);
  console.log(height.value);
  bmi.value = +weight.value/+height.value;
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
      <p>Current weight {{weight}} kg</p>
      <p>Current height {{height}} cm</p>
    </div>
  </div>

  <div>
    <h1>Calculate BMI</h1>
    <button @click="calculate()">Calculate</button>
    <div v-if="bmi < 25 " class="bmigreen">
      <p >{{bmi}}</p>
    </div>
    <div v-else-if="bmi < 30" class="bmiyellow">
      <p>{{bmi}}</p>
    </div>
    <div v-else class="bmired">
      <p >{{bmi}}</p>
    </div>

    <div>
      <h1>Weight History</h1>
      <ul>
        <li v-for="weights in weightList">
          {{weights}}
        </li>
      </ul>
    </div>
  </div>
</form>
</template>



<style scoped>

.bmigreen {
  background-color: green;
}

.bmired {
  background-color: red;
}

.bmiyellow {
  background-color: yellow;
}

</style>