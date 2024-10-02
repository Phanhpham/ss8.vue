<template>
    <form @submit.prevent="handleSubmit">
      <h2> Tien do:{{ progress }} %</h2>
      <div><input v-model="progress" type="range"/></div>
    </form>
  </template>
  
  <script setup>
  import { reactive, ref } from "vue";
  const progress = ref("");
  
 
  const handleSubmit = () => {
    // ngan chan su kien load lai trang
  
    // e.preventDefault();
    
  };
  </script>
  
  <style></style>
  