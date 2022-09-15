<template>
  <RouterView />
</template>

<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Cart from "./components/Cart.vue";
import Shop from "./components/Shop.vue";
</script>

<style lang="scss">
@import "./assets/base.scss";
@import "./assets/debug.scss";
</style>
