<template>
  <div>
    <navbar />
    <div id="app">
      <RentalForm />
    </div>
  </div>
</template>

<script setup>
import RentalForm from './components/RentalForm.vue';
import Navbar from './components/Navbar.vue';
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
