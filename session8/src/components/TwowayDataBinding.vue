<template>
  <form @submit.prevent="handleSubmit">
    <h3>Ten nguoi dung:{{ userInfo.userName }}</h3>
    <h2>DateOfBirth:{{ userInfo.dateOfBirth }}</h2>
    <h2>Gender:{{ userInfo.gender }}</h2>
    <h3>hobbie:{{ userInfo.hobbies }}</h3>
    <div>Ho va ten: <input v-model="userInfo.userName" type ="text" placeholder="nhap ten"/></div>
    <div>ngay sinh: <input v-model="userInfo.dateOfBirth" type="date"/></div>
    <div>Gioi tinh: </div>
    <div>
        Nam <input name="gender" v-model="userInfo.gender" type ="radio" value="0"/> 
        Nu <input name="gender" v-model="userInfo.gender" type ="radio" value="1"/>
         Khac <input name="gender" v-model="userInfo.gender" type ="radio" value="2"/>
    </div>
    <div>so thich</div>
    <div>
        choi game <input value="game" v-model ="userInfo.hobbies" type="checkbox"/>
        code <input value="code" v-model ="userInfo.hobbies" type="checkbox"/>
        boi loi  <input value="swim" v-model ="userInfo.hobbies" type="checkbox"/>
        bong chuyen <input value="voleyball" v-model ="userInfo.hobbies" type="checkbox"/>
    </div>
    <button>them</button>
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