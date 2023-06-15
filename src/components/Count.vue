<template>
  <div class="wrapper">
    <div v-if="todos.length == 0">Todo not Entered!</div>
    <div v-else class="bottom">
      <p><strong>Complated Todo:</strong>{{ trueCount }}</p>
      <p><strong>Pending Todo:</strong>{{ falseCount }}</p>
    </div>
  </div>
</template>

<script setup>
import { computed } from "vue";
import { useStore } from "vuex";

const store = useStore();

const todos = computed(() => store.state.todos);
const trueCount = computed(() => store.getters.getDoneTrue);
const falseCount = computed(() => store.getters.getDoneFalse);
</script>

<style scoped>
.wrapper {
  display: flex;
  justify-content: center;
  margin-top: 16px;
}
.bottom {
  display: flex;
  gap: 32px;
}
</style>
