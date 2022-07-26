<template>
  <div class="container-description pt-4">
      <div class="logo-container mt-3">
          <img src="../../../public/img/logo-restaurant-2x.png" alt="restaurant logo">
      </div>
      <CardForBanner  :txtForCard="txtForCard" />
  </div>
</template>

<script>
import CardForBanner from '../CardForBanner.vue'
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
  padding-left: 105px;
  width: 100%;
  height: 100%;
  .logo-container{
    height: 59px;
    margin-bottom: 50px;
    img{
      height: 100%;
    }
  }

}

</style>