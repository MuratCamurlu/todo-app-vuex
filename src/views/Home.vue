<template>
  <div class="home">
    <form @submit.prevent="userLogin">
      <div>
        <p>Name</p>
        <input type="text" required />
      </div>
      <div>
        <p>Email</p>
        <input type="email" required />
      </div>
      <button type="submit">Login</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";
const name = ref("");
const email = ref("");
const router = useRouter();
const userLogin = () => {
  router.push("/todo");
  name.value = "";
  email.value = "";
};
</script>

<style scoped>
.home {
  display: flex;
  justify-content: center;
  margin-top: 60px;
}
form {
  border: 1px solid grey;
  border-radius: 20px;
  padding: 16px;
  width: 60%;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 50px 100px -20px,
    rgba(0, 0, 0, 0.3) 0px 30px 60px -30px,
    rgba(10, 37, 64, 0.35) 0px -2px 6px 0px inset;
}
button {
  margin-top: 10px;
  background-color: green;
  color: white;
  padding: 5px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>
