<script setup>
// defineProps(["title"]);
const emits = defineEmits(["enlarge-text"]);
const props = defineProps(["pName", "title"]);
</script>
<template>
  <h4>{{ props.title }}</h4>
  <p>{{ props.pName }}</p>
  <button @click="emits('enlarge-text')">Enlarge Text</button>
  <slot />
</template>
