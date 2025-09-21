<template>
    <Button class="content__card-btn" @click="openPopup">
        Learn more
    </Button>
</template>

<script setup>
    import Button from '../../../Shared/ui/Button.vue';

    const emits = defineEmits('openPopup')

    const openPopup = function() {
        emits('openPopup', props.petModalContent.id)
    }
</script>

<style scoped>

</style>