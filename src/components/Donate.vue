<template>
    <div class="donate">
        <div class="donate__container">
            <img class="donate__dog-img" :src="DonateDogImg" alt="dog">
            <div class="donate__text">
                <h6 class="donate__title">
                    You can also make a donation
                </h6>
                <p class="donate__bankname">
                    Name of the bank / Type of bank account
                </p>
                <img :src="donateCardNumber" alt="cardnumber">
                <p class="donate__par">
                    Legal information and lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas a ipsum at libero sagittis dignissim sed ac diam. Praesent ultrices maximus tortor et vulputate. Interdum et malesuada fames ac ante ipsum primis in faucibus.
                </p>
            </div>
        </div>
    </div>
</template>

<script setup>
    import DonateDogImg from '../assets/images/DonateDogImg.png'
    import donateCardNumber from '../assets/images/donateCardNumber.png'
</script>

<style scoped>

.donate{
    padding-bottom: 100px;
    background-color: #FFFFFF;
}

.donate__container{
    margin-top: 80px;
    margin-bottom: 100px;
    margin-left: 463px;
    max-width: 915px;
    height: 282px;
    width: 100%;
    display: flex;
    justify-content: space-between;
}

.donate__dog-img{
    margin-top: 91px;
    max-width: 505px;
    width: 100%;
    height: 261px;
}

.donate__text{
    margin-left: 30px;
    max-width: 380px;
    width: 100%;
}

.donate__title{
    color: #545454;
    font-size: 35px;
    font-weight: 400;
    line-height: 130%;
    margin-bottom: 0;
    font-family: Georgia, sans-serif;
}

.donate__bankname{
    color: #545454;
    font-size: 15px;
    font-weight: 400;
    line-height: 110.00000000000001%;
    margin-bottom: 20px;
    font-family: Georgia, sans-serif;
}

.donate__par{
    color: #B2B2B2;
    font-size: 12px;
    font-weight: 400;
    line-height: 18px;
}

</style>