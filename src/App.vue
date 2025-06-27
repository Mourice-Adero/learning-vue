<script setup>
import SamplePerson from "./components/components-in-depth/SamplePerson.vue";
import ConditionalRendering from "./components/ConditionalRendering.vue";
import EventHandling from "./components/EventHandling.vue";
import FormInputBinding from "./components/FormInputBinding.vue";
import ReactivityFundamentals from "./components/ReactivityFundamentals.vue";
import Watchers from "./components/Watchers.vue";
</script>
<template>
  <h1>Learning Vue</h1>
  <div>
    <h3>Reactivity Fundamentals</h3>
    <ReactivityFundamentals />
    <br />
    <br />
    <h3>Form Input Binding</h3>
    <FormInputBinding />
    <br />
    <br />
    <h3>Event Handling</h3>
    <EventHandling />
    <br />
    <br />
    <h3>Conditional Rendering</h3>
    <ConditionalRendering />
    <br />
    <br />
    <h3>Watchers</h3>
    <Watchers />
    <br />
    <br />
    <h3>Components In Depth</h3>
    <SamplePerson />
  </div>
</template>
