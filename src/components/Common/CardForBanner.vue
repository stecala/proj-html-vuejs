<template>
  <div class="txt-container">
      <div class="subtitle text-uppercase position-relative">{{txtForCard.subtitle}}</div>
      <div class="title mt-4 text-uppercase">{{txtForCard.title}}</div>
      <div class="txt mt-4">{{txtForCard.text}}</div>
      <BtnApp :isWhite="isWhite" :element="txtForCard.btn.text_btn" :elementURL="txtForCard.btn.url" />
  </div>
</template>

<script>
import BtnApp from './BtnApp.vue'
export default {
  data : function(){
    return{
      isWhite : true,
    }
  },
  components:{
    BtnApp,
  },
  props : {
    txtForCard : Object,
  },
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

    .txt-container{
      padding-top: 105px;
      padding-left: 120px;
      color: $txtColorWhite;
      font-family: 'Bebas Neue', cursive;
      .subtitle{
        font-size: 1rem;
        font-family: 'Poppins', sans-serif;
      }
      .subtitle::before{
        content: '';
        width: 50px;
        height: 1px;
        position: absolute;
        bottom: 50%;
        left: -100px;
        background-color: $txtColorWhite;
      }
      .title{
        font-size: 6rem;
        line-height: 1.2;
      }
      .txt{
        padding-right: 20px;
        font-size: 1.2rem;
        line-height: 2;
        font-family: 'Ibarra Real Nova', serif;
      } 
    }
</style>