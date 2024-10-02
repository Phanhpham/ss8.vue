<template>
  <div>
    <h1>one way data binding</h1>
    <h3>userName:{{ userName }}</h3>
    <input type = "text" :value="userName"/>
    <button @click="handleChangeName">Change name</button>
  </div>
</template>

<script setup>
import { ref } from "vue";
const userName = ref("nguyen van a");

const handleChangeName = ()=>{
    userName.value="nguyen van a";
}
</script>

<style></style>
