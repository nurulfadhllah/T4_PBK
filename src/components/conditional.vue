<script setup>
import {ref} from 'vue'

const awesome = ref(true)

function toggle() {
    awesome.value = !awesome.value
}
</script>

<template>
    <h1>{{ awesome }}</h1>
    <button @click="toggle">Toggle</button>
    <h1 v-if="awesome"> Vue is awesome</h1>
    <h1 v-else>Vue is not awesome</h1>
</template>

