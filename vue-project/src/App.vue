<script setup>
import { ref } from 'vue'

const msg = "Hallo world"
const rawHtml = "<li>Daftar 1</li>"
const link = "YouTube.com"
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper'
}
let  a = 10
let b = 5
let c = a + b
</script>

<template>
  <div id="app">
    <span>{{ msg }}</span><br>
    <span v-html="rawHtml"></span><br>
    <span style="color: green">Ini Warna Hijau</span><br>
    <button :disabled="isButtonDisabled">Button</button><br>
    <a v-bind:href="url"> YouTube.com </a><br>
    bil1 = {{ a }}<br>
    bil2 = {{ b }}<br>
    hasil = bil1 + bil2 = {{ c }}
  </div>
</template>