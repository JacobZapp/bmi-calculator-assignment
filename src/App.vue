<script setup>

import BodyMassIndex from "./components/BodyMassIndex.vue";

import { ref } from 'vue'

// const bmi = weight / (height * height)

function calculatedBMI(bmi) {

  calculatedBMI.value = `Your BMI is: ${bmi}`
}

</script>

<template>

    <h1>Body Mass Index Calculator</h1>


  <BodyMassIndex
  v-on:stats="calculatedBMI"></BodyMassIndex>

  <p> {{ calculatedBMI }}</p>

</template>

<style scoped>

</style>
