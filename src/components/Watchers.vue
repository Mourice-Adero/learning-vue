<!-- <script setup>
import { onMounted, ref, watch } from "vue";

const users = ref();
const loading = ref(false);
const message = ref("");
const refresh = ref(0);

const fetchUsers = async () => {
  loading.value = true;
  message.value = "Loading...";

  try {
    const res = await fetch(`https://dummyjson.com/users/`);
    const data = await res.json();
    users.value = data.users;
    message.value = "Users loaded";
  } catch (error) {
    console.log("Couldn't connect to API: " + error);
    message.value = "Failed";
  } finally {
    loading.value = false;
  }
};
onMounted(() => {
  fetchUsers();
});

watch(refresh, (newValue) => {
  if (newValue) {
    fetchUsers();
  }
});
</script>
<template>
  <p>Users</p>
  <button @click="refresh++">Refresh</button>
  <div>{{ loading ? message : message }}</div>
  <br />
  <li v-for="user in users">{{ user.firstName + " " + user.lastName }}</li>
</template> -->

<script setup>
import { ref, watch } from "vue";
const names = ref(["John", "Peter", "Mike", "Jane"]);
const filteredNames = ref([]);
const searchName = ref("");
const message = ref("");

filteredNames.value = [...names.value];
watch(
  searchName,
  () => {
    filteredNames.value = names.value.filter((name) =>
      name.toLowerCase().includes(searchName.value.toLowerCase())
    );
    if (filteredNames.value.length === 0) {
      message.value = "No match found";
    } else {
      message.value = "";
    }
  },
  { immediate: true }
);
</script>
<template>
  <p>Search User:</p>
  <input v-model="searchName" />
  <ul>
    <p v-if="message">{{ message }}</p>
    <li v-for="name in filteredNames">{{ name }}</li>
  </ul>
</template>

<!-- The Above can be implemented simply using computed -->
