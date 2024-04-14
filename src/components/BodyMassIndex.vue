<script setup>
import { ref, watch } from 'vue'

// const emit = defineEmits([
//   height, weight
// ])



const height = ref('')
const weight = ref('')

const stats = [height, weight]


</script>

<template>
  <div id="BMI">
    <form>
    <h2> Enter your Height and Weight</h2>

      <label> Height in Meters: </label>
      <input v-model="height" type="text">

    <br>

      <label> Weight in Kilograms: </label>
      <input v-model="weight" type="text">

    <br>

    <button v-on:click="defineEmits([stats-entered])">Calculate</button>
    </form>




  </div>
</template>

<style scoped>

</style>
