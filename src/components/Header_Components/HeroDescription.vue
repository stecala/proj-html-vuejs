<template>
  <div class="container-description pt-4">
      <div class="logo-container ">
          <img src="/img/logo-restaurant-2x.png" alt="restaurant logo">
      </div>
      <div class="my-margin">
        <CardForBanner  :txtForCard="txtForCard" />
      </div>
  </div>
</template>

<script>
import CardForBanner from '../Common/CardForBanner.vue'
export default {
  components : {
    CardForBanner,
  },
  props :{
    txtForCard : Object,
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

.container-description{
  background-color: $blackBg;
  width: 100%;
  height: 100%;
  min-height: 100vh;
  .logo-container{
    width: 50%;
    height: 59px;
    margin-left: 70px;
    margin-top: 50px;
    img{
      width: 100%;
      height: 100%;
    }
  }

}

</style>