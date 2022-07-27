<template>
  <div class="container-lg mt-5 pt-5">
    <div class="col-6 img-container">
        <img src="/img/blog72x-1200x1375.jpg" alt="Girl cooking">
    </div>
    <div class="col-6 text-zone align-items center">
        <ReviewCard :element="textCardsReview.firstReview" />
    </div>
  </div>
</template>

<script>
import ReviewCard from './ReviewCard.vue'
export default {
  components : {
    ReviewCard,
  },
  data : function(){
    return {
      textCardsReview: {
        firstReview :{
          reviewer : 'meggy stewart',
          Journal : 'new york times',
          stars :  '5',
          txt : 'Non arcu mauris tortor ultrices mollis tellus euismod fermentum. Habitant amet tincidunt, id sapien accumsai, sed at. Mmalesuada ullamcorper amet. Pretium pretium dignissim nisi.',
          btn : {
            url : '#',
            text : 'read full article'
          } 
        },
        secondReview :{
          reviewer : 'mary maxey',
          Journal : 'the guardian',
          stars :  '5',
          txt : 'Non arcu mauris tortor ultrices mollis tellus euismod fermentum. Habitant amet tincidunt id sapien accumsan sed.',
          btn : {
            url : '#',
            text : 'read full article'
          } 
        },
        thirdReview :{
          reviewer : 'patrick monroe',
          Journal : 'globe and mail',
          stars :  '5',
          txt : 'Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Nulla porttitor accumsan tincidunt.',
          btn : {
            url : '#',
            text : 'read full article'
          } 
        },
      
      
      }
    }
  }
}
</script>

<style scoped lang="scss">
    .img-container{
        height: 700px;
        img{
            width: 100%;
        }
    }
</style>