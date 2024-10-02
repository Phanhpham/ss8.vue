<template>
    <form @submit.prevent="handleSubmit">
      
      <h3>so thich:{{ userInfo.hobbies }}</h3>
      <div>
          choi game <input value="game" v-model ="userInfo.hobbies" type="checkbox"/>
          code <input value="code" v-model ="userInfo.hobbies" type="checkbox"/>
          boi loi  <input value="swim" v-model ="userInfo.hobbies" type="checkbox"/>
          bong chuyen <input value="voleyball" v-model ="userInfo.hobbies" type="checkbox"/>
      </div>
    
    </form>
  </template>
  
  <script setup>
  import {reactive, ref} from "vue";
 
  const hobbies=ref([]);
  
  const userInfo=reactive({
    
      hobbies:[]
  })
  const handleSubmit=() =>{
      // ngan chan su kien load lai trang 
  
      // e.preventDefault();
      const user ={
         
          hobbies:hobbies.value
      };
      console.log("Submited:" ,user);
  }
  </script>
  
  <style>
  
  </style>