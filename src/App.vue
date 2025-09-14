<template>
  <div class="app">
    <Header/>
    <About/>
    <Content :petsModalContent="petsModalContent" @openPopup="openPopup"/>
    <Help/>
    <Donate/>
    <Footer/>
    <MyModal v-for="petModalContent in petsModalContent" v-show="petModalContent.modalShowStatus" :key="petModalContent.id" v-model:modalShowStatus="petModalContent.modalShowStatus">
      <PetModalContent :petModalContent="petModalContent" :key="petModalContent.id" @closePopup="closePopup"/>
    </MyModal>
  </div>
</template>

<script setup>
  import Header from './components/Header.vue';
  import About from './components/About.vue';
  import Content from './components/Content.vue';
  import { petsModalContent } from './data/petsInfo'
  import Help from './components/Help.vue';
  import Donate from './components/Donate.vue';
  import Footer from './components/Footer.vue';
  import MyModal from './components/UI/MyModal.vue';
  import PetModalContent from './components/PetModalContent.vue';

  const openPopup = function(popupID) {
    let currentPopup = petsModalContent.find(item => item.id === popupID);
    currentPopup.modalShowStatus = true;
  }

  const closePopup = function(popupID) {
    let currentPopup = this.petsModalContent.find(item => item.id === popupID);
    currentPopup.modalShowStatus = false;
  }
</script>

<style>

.app{
  max-width: 1920px;
  width: 100%;
  padding: 0;
  margin: 0;
  font-family: Arial, sans-serif;
}

</style>