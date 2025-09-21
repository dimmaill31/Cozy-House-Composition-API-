<template>
    <div class="content__card">
    <img :src="petModalContent.petImg" :alt="petModalContent.name">
        <p class="content__card-text">
            {{ petModalContent.name }}
        </p>
        <Button class="content__card-btn" @click="openPopup">
            Learn more
        </Button>
    </div>
</template>

<script setup>
    import Button from '../Shared/ui/Button.vue'
    const props = defineProps({
        petModalContent: {
            type: Object,
            required: true,
        }
    })

    const emits = defineEmits('openPopup')

    const openPopup = function() {
        emits('openPopup', props.petModalContent.id)
    }
</script>

<style scoped>

.content__card{
    max-width: 270px;
    width: 100%;
}

.content__card-text{
    margin-left: 94px;
    margin-top: 30px;
    margin-bottom: 30px;
    font-family: Georgia, sans-serif;
    font-weight: 400px;
    font-size: 20px;
    line-height: 100%;
    letter-spacing: 6%;
}

.content__card-btn{
    margin-left: 33px;
    max-width: 187px;
    width: 100%;
    border: 2px solid #F1CDB3;
    background-color: transparent;
    border-radius: 100px;
    padding: 15px 45px;
    margin-bottom: 30px;
    font-family: Georgia, sans-serif;
}

.content__card-btn:hover{
    background-color: #FDDCC4;
    cursor: pointer;
}

</style>