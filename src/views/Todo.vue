<template>
  <div>
    <Navbar />
  </div>
  <div>
    <AddTodo />
    <div>
      <Count />
    </div>
    <div>
      <ListTodo />
    </div>
  </div>
</template>
<script setup>
import Navbar from "@/components/Navbar.vue";
import AddTodo from "@/components/AddTodo.vue";
import Count from "@/components/Count.vue";
import ListTodo from "@/components/ListTodo.vue";
</script>

<style scoped></style>
