<template>
  <div class="app">
    <Header/>
    <About/>
    <Content :petsModalContent="petsModalContent" @openPopup="openPopup"/>
    <Help/>
    <Donate/>
    <Footer/>
    <Modal v-for="petModalContent in petsModalContent" v-show="petModalContent.modalShowStatus" :key="petModalContent.id" v-model:modalShowStatus="petModalContent.modalShowStatus">
      <PetModalContent :petModalContent="petModalContent" :key="petModalContent.id" @closePopup="closePopup"/>
    </Modal>
  </div>
</template>

<script setup>
  import Header from './Entities/Header/ui/Header.vue';
  import About from './Entities/About/ui/About.vue';
  import Content from './Widgets/Content/ui/Content.vue';
  import { petsModalContent } from './data/petsInfo'
  import Help from './Entities/Help/ui/Help.vue';
  import Donate from './Entities/Donate/ui/Donate.vue';
  import Footer from './components/Footer.vue';
  import Modal from './Shared/ui/Modal.vue';
  import PetModalContent from './Widgets/PetModalContent/ui/PetModalContent.vue';

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