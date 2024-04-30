<template>
  <div>
    <h1>Home</h1>
    <h2>{{ name }}</h2>
    <h3>{{ student.name }}</h3>
    <h3>{{ student.school }}</h3>
    <button @click="changeName">Change Name</button>
    <p>This is the home page</p>
    <router-Link to="/about">About Page</router-Link>
  </div>
</template>

<script setup>
import { ref, reactive } from "@vue/reactivity";

const name = ref("Yinka");

console.log(name);

const student = reactive({
  name: "Yinka",
  school: "Alt School",
});

const changeName = () => {
  name.value = "Kadiri Adeyinka";
};
</script>
