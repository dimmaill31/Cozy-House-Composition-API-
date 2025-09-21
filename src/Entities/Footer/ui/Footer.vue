<template>
    <div class="footer">
        <div class="footer__container">
            <div class="footer__contacts">
                <h6 class="footer__contacts-title">
                    For questions and suggestions
                </h6>
                <div class="footer__contacts-btns">
                    <MyButton class="footer__email">
                        <img :src="FooterMailImg" alt="email">
                    </MyButton>
                    <MyButton class="footer__phone">
                        <img :src="footerPhoneImg" alt="phone">
                    </MyButton>
                </div>
            </div>
            <div class="footer__place">
                <h6 class="footer__where">
                    We are waiting for your visit
                </h6>
                <div>
                    <MyButton class="footer__boston">
                        <img :src="footerBostonImg" alt="boston">
                    </MyButton>
                    <MyButton class="footer__london">
                        <img :src="footerLondonImg" alt="london">
                    </MyButton>
                </div>
            </div>
            <img class="footer__dog" :src="footerDogImg" alt="dog">
        </div>
    </div>
</template>

<script setup>
    import FooterMailImg from '../assets/images/FooterMailImg.png'
    import footerPhoneImg from '../assets/images/footerPhoneImg.png'
    import footerBostonImg from '../assets/images/footerBostonImg.png'
    import footerLondonImg from '../assets/images/footerLondonImg.png'
    import footerDogImg from '../assets/images/footerDogImg.png'
    import MyButton from '../Shared/ui/Button.vue'
</script>

<style scoped>

.footer{
    background-image: url(../assets/images/footerBackground.png);
    height: 350px;
    padding-left: 40px;
}

.footer__container{
    display: flex;
    justify-content: space-between;
}

.footer__contacts{
    margin-bottom: 60px;
    max-width: 278px;
    width: 100%;
    padding-bottom: 0;
}

.footer__contacts-title{
    color: #FFFFFF;
    font-size: 35px;
    font-weight: 400;
    line-height: 130%;
}

.footer__phone{
    margin-top: 40px;
}

.footer__place{
    margin-bottom: 60px;
    max-width: 278px;
    width: 100%;
    padding-bottom: 0;
}

.footer__where{
    color: #FFFFFF;
    font-size: 35px;
    font-weight: 400;
    line-height: 130%;
}

.footer__dog{
    height: 310px;
    width: 300px;
    padding-right: 40px;
    padding-top: 40px;
}

</style>