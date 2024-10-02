<template>
    <form @submit.prevent="handleSubmit">
        <h1>Color </h1>
      
      <input v-model="selectedColor" type ="color" />
    <h3>Ma mau : <strong>{{ selectedColor }}</strong></h3>
      
    </form>
  </template>
  
  <script setup>
  import {reactive, ref} from "vue";
  const selectedColor=ref("")
  
  
  
  </script>
  
  <style>
  
  </style>