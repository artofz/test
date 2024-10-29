<template>
  <button @click="test()">test</button>
  <!--  <button @click="account()">account</button>-->
  <!--  <button @click="login()">login</button>-->
  <!--  <button @click="session()">getSession</button>-->
</template>

<script setup>
import axios from "axios";

let cookie;

const test = async () => {
  const response = await axios.get("http://localhost:2020/v1/ban_users")
  console.log(response)
}

const login = async () => {
  const response = await axios.post("http://localhost:8088/login", {
    "reqBody": "fram@futurewiz.co.kr"
  });
  console.log(document.cookie)
  console.log(response)
}

const account = async () => {
  const response = await axios.get("http://localhost:8088/account", {
    withCredentials: true,
  })
  console.log(response)
}

const session = async () => {
  const response = await axios.get("http://localhost:8088/session", {
  })

  console.log(response)
}
</script>