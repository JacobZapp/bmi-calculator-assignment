<script setup>
import { ref, watch } from 'vue'

const emit = defineEmits([
 'stats-entered'
])

function onStatsEntered() {
  emit('stats-entered', height.value, weight.value)
}

const height = ref('')
const weight = ref('')

const stats = [height, weight]


</script>

<template>
  <div id="BMI">

    <h2> Enter your Height and Weight</h2>

      <label> Height in Meters: </label>
      <input v-model="height" type="text">

    <br>

      <label> Weight in Kilograms: </label>
      <input v-model="weight" type="text">

    <br>

    <button v-on:click='onStatsEntered'>Calculate</button>





  </div>
</template>

<style scoped>

</style>
