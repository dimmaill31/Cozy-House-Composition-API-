<template>
    <div class="about">
        <div class="about__container">
            <img class="about__dogs-img">
            <div class="about__text">
                <h4 class="about__title">
                    About the shelter “Cozy House”
                </h4>
                <p class="about__subtitle">
                    Currently we have 121 dogs and 342 cats on our hands and statistics show that only 20% of them will find a family. The others will continue to live with us and will be waiting for a lucky chance to become dearly loved.
                </p>
                <p class="about__subtitle">
                    We feed our wards with the best food and make sure that they do not get sick, feel comfortable (including psychologically) and well. We are supported by 87 volunteers and 28 employees of various skill levels. About 12% of the animals are taken by the shelter staff. Taking care of the animals, they become attached to the pets and would hardly ever leave them alone.
                </p>
            </div>
        </div>
    </div>
</template>

<script setup>
    
</script>

<style scoped>

.about__container{
    margin-top: 80px;
    margin-left: 320px;
    margin-bottom: 100px;
    max-width: 1200px;
    width: 100%;
    display: flex;
}

.about__dogs-img{
    margin-left: 175px;
}

.about__text{
    margin-left: 120px;
    margin-top: 14px;
    align-items: center;
    justify-content: space-between;
}

.about__title{
    color: #545454;
    font-size: 35px;
    font-weight: 400;
    line-height: 130%;
}

.about__subtitle{
    color: #4C4C4C;
    font-size: 15px;
    font-weight: 400;
    line-height: 160%;
}

</style>