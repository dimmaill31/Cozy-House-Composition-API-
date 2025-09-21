<template>
    <div class="modal__content">
        <img clas="modal__pet-img" :src="petModalContent.petImg" :alt="petModalContent.name">
        <div class="modal__container">
            <h2 class="modal__name">
                {{ petModalContent.name }}
            </h2>
            <h3 class="modal__breed">
                {{ petModalContent.breed }}
            </h3>
            <p class="modal__text">
                {{ petModalContent.text }}
            </p>
            <ul class="modal__infos">
                <li class="modal__info">
                    Age:
                    <p class="modal__meaning">
                        {{ petModalContent.age }}
                    </p>
                </li>
                <li class="modal__info">
                    Inoculations:
                    <p class="modal__meaning">
                        {{ petModalContent.inoculations }}
                    </p>
                </li>
                <li class="modal__info">
                    Diseases:
                    <p class="modal__meaning">
                        {{ petModalContent.diseases }}
                    </p>
                </li>
                <li class="modal__info">
                    Parasites:
                    <p class="modal__meaning">
                        {{ petModalContent.parasites }}
                    </p>
                </li>
            </ul>
        </div>
        <MyButton class="modal__close-btn" @click="closePopup">
            <img :src="popupCloseBtn" alt="close">
        </MyButton>
    </div>
</template>

<script setup>
    import MyButton from '../Shared/ui/Button.vue';
    import popupCloseBtn from '../assets/images/popupCloseBtn.png'

    const props = defineProps({
        petModalContent: {
            type: Object,
            required: true,
        }
    })

    const emits = defineEmits('closePopup')

    const closePopup = function() {
        emits('closePopup', this.petModalContent.id)
    }
</script>

<style scoped>

.modal__content{
    padding: 190px;
    background-color: #FAFAFA;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    max-width: 900px;
    width: 100%;
    border-radius: 9px;
}

.modal__pet-img{
    max-width: 500px;
    width: 100%;
}

.modal__container{
    margin-left: 30px;
    display: block;
    max-width: 350px;
    width: 100%;
}

.modal__name{
    color: #000000;
    font-size: 35px;
    font-weight: 400;
    line-height: 130%;
}

.modal__breed{
    margin-top: 10px;
    color: #000000;
    font-size: 20px;
    font-weight: 400;
    line-height: 114.99999999999999%;
}

.modal__text{
    margin-top: 40px;
    color: #000000;
    font-size: 15px;
    font-weight: 400;
    line-height: 110.00000000000001%;
    margin-bottom: 40px;
}

.modal__infos{
    color: black;
    font-weight: 400;
    font-size: 15px;
}

.modal__close-btn{
    border: 2px solid #F1CDB3;
    border-radius: 100px;
    background-color: transparent;
    padding: 20px;
}

.modal__close-btn:hover{
    background-color: #FDDCC4;
    transition: opacity 0.3s ease;
    cursor: pointer;
}

</style>