<template>
    <div class="content">
        <div class="content__container">
            <h5 class="content__title">
                Our friends who are looking for a house
            </h5>
            <div class="content__subcontainer">
                <MyButton class="content__left-btn">
                    <img :src="contentLeftBtn" alt="left">
                </MyButton>
                <ContentCards :petsModalContent="petsModalContent" @openPopup="openPopup"/>
                <MyButton class="content__right-btn">
                    <img :src="contentRightBtn" alt="right">
                </MyButton>
            </div>
            <MyButton class="content__btn">
                Get to know the rest
            </MyButton>
        </div>
    </div>
</template>

<script setup>
    import ContentCards from './ContentCards.vue'
    import MyButton from './UI/MyButton.vue'
    import contentLeftBtn from '../assets/images/contentLeftBtn.png'
    import contentRightBtn from '../assets/images/contentRightBtn.png'

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

.content__container{
    margin-top: 80px;
    margin-bottom: 100px;
    margin-left: 320px;
    margin-right: 360px;
    max-width: 1200px;
    width: 100%;
    display: block;
}

.content__title{
    margin-left: 400px;
    color: #545454;
    font-size: 35px;
    font-weight: 400;
    line-height: 130%;
    max-width: 400px;
    width: 100%;
    text-align: center;
}

.content__subcontainer{
    display: flex;
    padding-bottom: 60px;
    margin: 0;
}

.content__left-btn{
    margin-top: 192px;
    height: 52px;
}

.content__left-btn:hover{
    background-image:  url(../assets/images/contentLeftBtnOnHover.png);
    transition: opacity 0.3s ease;
    cursor: pointer;
}

.content__btn{
    color: #292929;
    background-color: #F1CDB3;
    border-radius: 100px;
    padding: 15px 45px;
    font-size: 17px;
    font-weight: 400;
    line-height: 130%;
    margin-left: 480px;
}

.content__btn:hover{
    background-color: #FDDCC4;
    transition: opacity 0.3s ease;
    cursor: pointer;
}

.content__right-btn{
    margin-top: 192px;
    height: 52px;
    margin-left: 53px;
}

.content__right-btn:hover{
    background-image: url(../assets/images/contentRightBtnOnHover.png);
    transition: opacity 0.3s ease;
    cursor: pointer;
}

</style>