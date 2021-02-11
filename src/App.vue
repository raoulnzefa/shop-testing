<template>
  <NavBar />

  <HomePage />
</template>

<script setup>
import NavBar from "./components/NavBar.vue";
import HomePage from "./components/HomePage.vue";
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>