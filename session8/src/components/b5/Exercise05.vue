<template>
  <form @submit.prevent="handleSubmit">
    <h2>Gioi tinh:{{ gender }}</h2>
    <div>
      Nam
      <input name="gender" v-model="gender" type="radio" value="nam" /><br>
      Nu
      <input name="gender" v-model="gender" type="radio" value="nu" /><br>
      Khac
      <input name="gender" v-model="gender" type="radio" value="khac" />
    </div>
  </form>
</template>

<script setup>
import { ref } from "vue";
const gender = ref("");
</script>

<style></style>
