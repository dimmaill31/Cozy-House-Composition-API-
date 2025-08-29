<template>
    <div class="header">
      <div class="header__container">
        <div class="header__logo">
          <h2 class="header__title">Cozy House</h2>
          <p class="header__subtitle">Shelter for pets in Boston</p>
        </div>
        <nav class="header__navigates">
          <MyButton class="header__nav">
            About the shelter
          </MyButton>
          <MyButton class="header__nav">
            Our pets
          </MyButton>
          <MyButton class="header__nav">
            Help the shelter
          </MyButton>
          <MyButton class="header__nav">
            Contacts
          </MyButton>
        </nav>
      </div>
      <div class="body">
        <div class="body__main">
          <div class="body__info">
            <h3 class="body__title">Not only people need a house</h3>
            <p class="body__subtitle">We offer to give a chance to a little and nice puppy with an extremely wide and open heart. He or she will love you more than anybody else in the world, you will see!</p>
            <MyButton class="body__btn">
              Make a friend
            </MyButton>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  import MyButton from './UI/MyButton.vue'

</script>

<style scoped>

.header{
  background-image: url(../assets/images/backgroundHeader1920.png);
  margin: 0;
  padding-top: 30px;
  background-size: cover;
  font-family: Georgia, serif;
}

.header__container{
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  max-width: 1280px;
  width: 100%;
}

.header__navigates{
  display: flex;
  justify-content: space-between;
  max-width: 443px;
  width: 100%;
  color: #FAFAFA;
}

.header__title{
  margin: 0;
  color:#F1CDB3;
  font-size: 32px;
  font-weight: 400;
  line-height: 110.00000000000001%;
}

.header__subtitle{
  margin: 0;
  color: #FFFFFF;
  font-size: 13px;
  font-weight: 400;
  line-height: 100%;
  margin-top: 10px;
}

.body{
  font-family: Georgia, serif;
  display: flex;
}

.body__main{
  margin-top: 90px;
  margin-left: 320px;
  max-width: 460px;
  width: 100%;

}

.body__info{
  margin-top: 163px;
  padding-bottom: 243px;
  display: block;
}

.body__title{
  color: #FFFFFF;
  font-size: 44px;
  font-weight: 400;
  line-height: 130%;
}

.body__subtitle{
  color: #CDCDCD;
  font-size: 15px;
  font-weight: 400;
  line-height: 160%;
  margin-bottom: 42px;
  margin-right: 42px;
}

.body__btn{
  color: #292929;
  padding: 15px 45px;
  background-color: #F1CDB3;
  border: 0;
  border-radius: 100px;
}

.body__btn:hover {
  background-color: #FDDCC4;
  transition: opacity 0.3s ease;
  cursor: pointer;
}

</style>