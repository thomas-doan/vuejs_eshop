<template>
  <h2>form</h2>
  <input ref="input" type="text" placeholder="Nom" />

  <ul>
    <li ref="fruitsRef" v-for="fruit of arr" :key="fruit">{{ fruit }}</li>
  </ul>
  <RouterView />
</template>

<script setup lang="ts">
import { onMounted, reactive, ref } from "vue";
import { RouterLink, RouterView } from "vue-router";

const input = ref<HTMLInputElement | null>(null);
const arr = reactive(["pomme", "poire", "orange"]);
const fruitsRef = ref<HTMLInputElement[] | []>([]);

onMounted(() => {
  input.value?.focus();
  console.log(fruitsRef.value);
});
</script>

<style scoped></style>
