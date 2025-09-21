<template>
    <div class="content">
        <div class="content__container">
            <h5 class="content__title">
                Our friends who are looking for a house
            </h5>
            <div class="content__subcontainer">
                <Button class="content__left-btn">
                    <img :src="contentLeftBtn" alt="left">
                </Button>
                <PetsGallery class="contentCards" :petsModalContent="petsModalContent" @openPopup="openPopup"/>
                <Button class="content__right-btn">
                    <img :src="contentRightBtn" alt="right">
                </Button>
            </div>
            <Button class="content__btn">
                Get to know the rest
            </Button>
        </div>
    </div>
</template>

<script setup>
    import Button from '../Shared/ui/Button.vue'
    import contentLeftBtn from '../assets/images/contentLeftBtn.png'
    import contentRightBtn from '../assets/images/contentRightBtn.png'
    import PetsGallery from '../../PetsGallery/ui/PetsGallery.vue'

    const props = defineProps({
        petsModalContent:{
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

.content{
    background-color: #F6F6F6;
}

.content__container{
    padding-top: 80px;
    padding-bottom: 100px;
    padding-left: 320px;
    max-width: 1200px;
    width: 100%;
    display: block;
}

.content__title{
    margin: 0;
    margin-left: 400px;
    margin-right: 400px;
    margin-bottom: 60px;
    color: #545454;
    font-size: 35px;
    font-weight: 400;
    line-height: 130%;
    letter-spacing: 6%;
    max-width: 400px;
    width: 100%;
    text-align: center;
    font-family: Georgia, sans-serif;
    max-width: 400px;
    width: 100%;
}

.content__subcontainer{
    display: flex;
    padding-bottom: 60px;
    justify-content: space-between;
}

.content__left-btn{
    padding: 0;
    margin-top: 192px;
    height: 52px;
    margin-right: 53px;
    max-width: 52px;
    width: 100%;
    background-color: transparent;
    border: none;
}

.content__left-btn:hover{
    background-image:  url(../assets/images/contentLeftBtnOnHover.png);
    transition: opacity 0.3s ease;
    cursor: pointer;
}

.contentCards{
    display: flex;
    max-width: 990px;
    width: 100%;
    justify-content: space-between;
}

.content__btn{
    color: #292929;
    background-color: #F1CDB3;
    border-radius: 100px;
    border: none;
    padding: 15px 45px;
    font-size: 17px;
    font-weight: 400;
    line-height: 130%;
    margin-left: 480px;
    font-family: Georgia, sans-serif;
}

.content__btn:hover{
    background-color: #FDDCC4;
    transition: opacity 0.3s ease;
    cursor: pointer;
}

.content__right-btn{
    padding: 0;
    margin-top: 192px;
    height: 52px;
    margin-left: 53px;
    max-width: 52px;
    width: 100%;
    background-color: transparent;
    border: none;
}

.content__right-btn:hover{
    background-image: url(../assets/images/contentRightBtnOnHover.png);
    transition: opacity 0.3s ease;
    cursor: pointer;
}

</style>