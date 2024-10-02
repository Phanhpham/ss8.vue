<template>
  <form @submit.prevent="handleSubmit">
    <h2>Ngay sinh:{{ userInfo.dateOfBirth }}</h2>
    <div><input v-model="userInfo.dateOfBirth" type="date"/></div>
  </form>
</template>

<script setup>
import { reactive, ref } from "vue";
const dateOfBirth = ref("");

const userInfo = reactive({
  dateOfBirth: "",
});
const handleSubmit = () => {
  // ngan chan su kien load lai trang

  // e.preventDefault();
  const user = {
    dateOfBirth: dateOfBirth.value,
  };
  console.log("Submited:", user);
};
</script>

<style></style>
