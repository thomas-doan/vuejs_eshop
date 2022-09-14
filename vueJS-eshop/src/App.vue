<template>
  <header>
    <input
      class="input"
      :class="{
        inputOnGoing: inputOnGoing,

        //synthaxe plus rapide
        inputError,
        inputValid,
      }"
      @focus="
        focus = true;
        touched = true;
      "
      @blur="focus = false"
      type="text"
      v-model="input"
    />
  </header>

  <RouterView />
</template>

<script setup lang="ts">
import { computed, ref } from "vue";
import { RouterLink, RouterView } from "vue-router";

//ref permet de la réactivité uniquement sur des primitives
const input = ref("");

//permet d'écouter le focus ou pas et en fonction assigné une nouvelle classe
const focus = ref(false);

const Valid = ref(false);

const touched = ref(false);

//computed permet d'actualiser
const inputOnGoing = computed(() => focus.value && input.value.length);

const inputValid = computed(() => !inputError.value && !focus.value);

const inputError = computed(
  () => !focus.value && touched.value && input.value.length < 6
);
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

.inputError {
  border-color: red;
}

.inputValid {
  border-color: green;
}
</style>
