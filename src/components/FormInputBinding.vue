<script setup>
import { ref } from "vue";
const manualMessage = ref("");
const modelMessage = ref("");
const textMessage = ref("");
const isJohn = ref(false);
const checkedNames = ref([]);
</script>
<template>
  <!-- Manual value binding -->
  <p>Manual: value is: {{ manualMessage }}</p>
  <input
    :value="manualMessage"
    @input="(event) => (manualMessage = event.target.value)"
    placeholder="manual binding"
  />
  <br />
  <!-- v-model directive -->
  <p>v-model directive: value is: {{ modelMessage }}</p>
  <input v-model.trim="modelMessage" placeholder="v-model directive" /><br />
  <p>v-model directive: value is: {{ textMessage }}</p>
  <br />
  <textarea v-model="textMessage"></textarea>

  <!-- Checkbox -->
  <br />
  <p>Is John checked?</p>
  <input type="checkbox" id="john" v-model="isJohn" />
  <label for="john">{{ isJohn }}</label>

  <!-- <ultiple checks -->
  <br />
  <p>Checked names: {{ checkedNames }}</p>
  <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
  <label for="jack">Jack</label>

  <input type="checkbox" id="john" value="John" v-model="checkedNames" />
  <label for="john">John</label>

  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
  <label for="mike">Mike</label>
</template>
