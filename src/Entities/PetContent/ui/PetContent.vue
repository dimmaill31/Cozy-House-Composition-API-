<template>
    <div class="content__card">
    <img :src="petModalContent.petImg" :alt="petModalContent.name">
        <p class="content__card-text">
            {{ petModalContent.name }}
        </p>
    </div>
</template>

<script setup>
    const props = defineProps({
        petModalContent: {
            type: Object,
            required: true,
        }
    })
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