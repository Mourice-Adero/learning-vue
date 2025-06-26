<script setup>
//Declaring reactive state
import { ref } from "vue";

// const users = reactive({}) --- Only works with state for object types
const count = ref(0);
console.log(count); // {value: 0}
console.log(count.value); // 0
</script>

<template>
  <p>Increment</p>
  <button @click="count++">add 1</button>
  <p>Count = {{ count }}</p>
</template>

<!-- Manually Exposing state Without using <script setup> -->
<!-- <script>
import { ref } from "vue";

export default {
  setup() {
    const count = ref(0);

    function increment() {
      count.value++;
    }

    return {
      count,
      increment,
    };
  },
};
</script>

<template>
  <p>Increment</p>
  <button @click="count++">add 1</button>
  <p>Count = {{ count }}</p>
</template> -->
