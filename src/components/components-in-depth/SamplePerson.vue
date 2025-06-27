<script setup>
import { ref } from "vue";
import PassingProps from "./PassingProps.vue";

const nameFontSize = ref(1);
</script>

<template>
  <div :style="{ fontSize: nameFontSize + 'em' }">
    <PassingProps
      title="Manager"
      pName="John Doe"
      @enlarge-text="nameFontSize += 0.1"
    />
  </div>
  <div :style="{ fontSize: nameFontSize + 'em' }">
    <PassingProps title="Orgernizer" pName="Jane Doe"
      ><p>Costom content</p></PassingProps
    >
  </div>
</template>
