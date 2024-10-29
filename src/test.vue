<template>
  <button @click="request()">button</button>
</template>

<script setup>
import axios from "axios";

const request = async () => {
  const response = await axios.get("http://localhost:8088/login");
  console.log(response)
}
</script>