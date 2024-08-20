<script setup>
import { ref } from 'vue'

const url = 'https://en.wikipedia.org/w/api.php?origin=*&action=query&format=json&meta=userinfo&formatversion=2&uiprop=rights'
const data = ref(null)
const error = ref(null)

function getUserInfo() {
  fetch(url)
    .then((res) => res.json())
    .then((json) => (data.value = json))
    .catch((err) => (error.value = err))
    console.log(data.value)
  }
</script>


<template>
  <main>
    <button @click="getUserInfo">UserInfo!</button>
    <p>
      {{ data }}
    </p>
  </main>
</template>
