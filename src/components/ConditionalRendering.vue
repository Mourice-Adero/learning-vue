<script setup>
import { ref } from "vue";

const user = ref({});
const message = ref("Hello World");
</script>
<template>
  <div>
    <p>Check User Availability</p>
    <i>is user available?: </i><span v-if="user">Yes</span
    ><span v-else="!user">No</span>
    <br />
    <i>User's message is: </i
    ><span>{{ message ? message : "No message" }}</span>
  </div>
</template>
