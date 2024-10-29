<template>
  <button @click="request()">button</button>
</template>

<script setup>
import axios from "axios";

const request = async () => {
  const response = await axios.get("https://192.168.3.73:9010/v1/extract_stock/mobile?catchType=best");
  console.log(response)
}
</script>