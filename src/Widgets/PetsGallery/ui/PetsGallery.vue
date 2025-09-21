<template>
    <div>
        <Swiper class="content__cards" :slides-per-view="3" :space-between="0">
            <SwiperSlide v-for="petModalContent in petsModalContent" :key="petModalContent.id">
                <PetCard :key="petModalContent.id" :petModalContent="petModalContent" @openPopup="openPopup"/>
            </SwiperSlide>
        </Swiper>
    </div>
</template>

<script setup>
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import 'swiper/css';
    import 'swiper/css/navigation';
    import PetCard from '../../PetCard/ui/PetCard.vue';

    const props = defineProps({
        petsModalContent: {
            type: Array,
            required: true,
        }
    })

    const emits = defineEmits('openPopup')

    const openPopup = function(popupID) {
        emits('openPopup', popupID)
    }
</script>

<style scoped>

.content__cards{
    padding-top: 60px;
    padding-left: 53px;
    display: flex;
    max-width: 990px;
    width: 100%;
    justify-content: space-between;
    background-color: #FAFAFA;
}

</style>