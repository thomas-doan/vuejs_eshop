<template>
  <RouterView />
  <div>
    <Header>
      <h1>Header</h1>
    </Header>
  </div>
</template>

<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<style lang="scss" scoped></style>
