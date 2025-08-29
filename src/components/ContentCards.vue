<template>
    <div>
        <Swiper class="content__cards" :slides-per-view="3" :space-between="0">
            <SwiperSlide v-for="petModalContent in petsModalContent" :key="petModalContent.id">
                <ContentCard :key="petModalContent.id" :petModalContent="petModalContent" @openPopup="openPopup"/>
            </SwiperSlide>
        </Swiper>
    </div>
</template>

<script setup>
    import ContentCard from './ContentCard.vue';
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import 'swiper/css';
    import 'swiper/css/navigation';

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
    max-width: 1094px;
    width: 100%;
    justify-content: space-between;
}

</style>