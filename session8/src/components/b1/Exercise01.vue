<template>
    <form @submit.prevent="handleSubmit">
        <h1>Email </h1>
      
      <input v-model="userInfo.userName" type ="text" placeholder="nhap email"/>
    <h3>Gia tri : {{ userInfo.userName }}</h3>
      
    </form>
  </template>
  
  <script setup>
  import {reactive, ref} from "vue";
  const dateOfBirth=ref("")
  const userName=ref("")
  const gender=ref("")
  const hobbies=ref([]);
  
  const userInfo=reactive({
      userName:"",
      dateOfBirth:"",
      gender:"0",
      hobbies:[]
  })
  const handleSubmit=() =>{
      // ngan chan su kien load lai trang 
  
      // e.preventDefault();
      const user ={
          userName:userName.value,
          dateOfBirth:dateOfBirth.value,
          gender:gender.value,
          hobbies:hobbies.value
      };
      console.log("Submited:" ,user);
  }
  </script>
  
  <style>
  
  </style>