<template>
    <div class="content__card">
    <img :src="petModalContent.petImg" :alt="petModalContent.name">
        <p class="content__card-text">
            {{ petModalContent.name }}
        </p>
        <MyButton class="content__card-btn" @click="openPopup">
            Learn more
        </MyButton>
    </div>
</template>

<script setup>
    import MyButton from './UI/MyButton.vue'
    const props = defineProps({
        petModalContent: {
            type: Object,
            required: true,
        }
    })

    const emits = defineEmits('openPopup')

    const openPopup = function() {
        emits('openPopup', this.petModalContent.id)
    }
</script>

<style scoped>

</style>