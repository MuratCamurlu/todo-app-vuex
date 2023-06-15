<template>
  <div class="wrapper">
    <p>Logo</p>
    <button @click="router.push('/')">Logout</button>
  </div>
</template>

<script setup>
import { useRouter } from "vue-router";

const router = useRouter();
</script>

<style scoped>
.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  border-bottom: 1px soid grey;
  height: 32px;
  background-color: rgb(221, 220, 220);
}
p {
  margin-left: 32px;
}
button {
  margin-right: 32px;
  background-color: black;
  color: white;
  border-radius: 5px;
  border: none;
  padding: 3px;
  cursor: pointer;
}
</style>
