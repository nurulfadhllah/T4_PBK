<script setup>
import {ref} from 'vue'

const titleClass = ref('title')

</script>

<template>
    <h1 :class="titleClass">Hari ini saya puasa</h1>
</template>

<style>
.title {
    color : red;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 20px;
}
</style>