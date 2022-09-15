<template>
  <RouterView />
  <div>
    <footer>
      <h1>Footer</h1>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<style lang="scss" scoped></style>
