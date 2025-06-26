<script setup>
import { ref } from "vue";
const name = ref("John Doe");
const greet = (event) => {
  alert(`Hello ${name.value}`);
};
</script>

<template>
  <!-- Method handler -->
  <p>{{ name }}</p>
  <button @click="greet">Greet</button>
  <!-- inline handler -->
  <button @click="() => console.log('clicked!')">Click Me</button>
</template>
