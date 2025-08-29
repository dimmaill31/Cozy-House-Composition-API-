<template>
  <div class="app">
    <Header/>
    <About/>
    <Content :petsModalContent="petsModalContent"/>
  </div>
</template>

<script setup>
  import Header from './components/Header.vue';
  import About from './components/About.vue';
  import Content from './components/Content.vue';
  import { petsModalContent } from './data/petsInfo'
</script>

<style scoped>

*{
  max-width: 1920px;
  width: 100%;
  padding: 0;
  margin: 0;
  font-family: Georgia, sans-serif;
}

</style>