<script setup>
import {ref} from 'vue'

let id = 1

const newInput = ref('')
const inputs = ref([
  { id: id++, text: 'Learn HTML', done: true },
  { id: id++, text: 'Learn JavaScript', done: true },
  { id: id++, text: 'Learn Vue', done: false }
])

function addInput() {
  inputs.value.push({ id: id++, text: newInput.value})
  newInput.value = ''
}

function removeInput(input) {
  inputs.value = inputs.value.filter((t) => t !== input)
}
</script>

<template>

  <form @submit.prevent="addInput">
    <input v-model="newInput" required placeholder="new input">
    <button>Add Input</button>
  </form>
  <ul>
    <li v-for="input in inputs" :key="input.id">
      {{ input.id }}. {{ input.text }}
      <button @click="removeInput(input)">X</button>
    </li>
  </ul>
</template>