<template>
    <div class="help">
        <div class="help__container">
            <h6 class="help__title">
                How you can help our shelter
            </h6>
            <img class="help__helplist" :src="HelpListImg" alt="helplist">
        </div>
    </div>
</template>

<script setup>
    import HelpListImg from "../assets/images/HelpListImg.png"
</script>

<style scoped>

.help__container{
    margin-top: 80px;
    margin-left: 320px;
    margin-bottom: 100px;
}

.help__title{
    margin-left: 446px;
    max-width: 308px;
    width: 100%;
    text-align: center;
    color: #545454;
    font-size: 35px;
    font-weight: 400;
    line-height: 130%;
    letter-spacing: 6%;
    font-family: Georgia, sans-serif;
}

.help__helplist{
    margin-left: 87px;
}

</style>