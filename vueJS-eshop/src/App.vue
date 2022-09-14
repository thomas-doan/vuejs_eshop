<template>
  <header>
    <input
      class="input"
      :class="{
        inputOnGoing: inputOnGoing,
      }"
      type="text"
      v-model="input"
    />
  </header>

  <RouterView />
</template>

<script setup lang="ts">
import { computed, ref } from "vue";
import { RouterLink, RouterView } from "vue-router";

const input = ref("");
const inputOnGoing = computed(() => input.value.length);
</script>

<style scoped>
.input {
  outline: 0;
  border: 1px solid black;
  border-radius: 4px;
}

.inputOnGoing {
  border-color: blue;
}
</style>
