<script setup>

import BodyMassIndex from "./components/BodyMassIndex.vue";

import { ref } from 'vue'



function calculatedBMI(height, weight) {
  const bmi = weight / (height * height)
  finalBMI.value = `Your BMI is: ${bmi}`
}

const finalBMI = ref()


</script>

<template>

    <h1>Body Mass Index Calculator</h1>


 <BodyMassIndex v-on:stats-entered="calculatedBMI"></BodyMassIndex>

  <p> {{ finalBMI }}</p>

</template>

<style scoped>

</style>
