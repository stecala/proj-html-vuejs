<template>
  <div class="container-lg mt-5 pt-3">
    <div class="row">
      <div class="col-6 img-container">
          <img src="/img/blog72x-1200x1375.jpg" alt="Girl cooking">
      </div>
      <div class="col-6 text-zone d-flex align-items-center card-container justify-content-center">
          <ReviewCard :element="textCardsReview.firstReview" />
      </div>
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
          journal : 'new york times',
          stars :  5,
          txt : {
            paragraph1 : 'Non arcu mauris tortor ultrices mollis tellus euismod fermentum. Habitant amet tincidunt, id sapien accumsai, sed at.' ,
            paragraph2 : 'Mmalesuada ullamcorper amet. Pretium pretium dignissim nisi.'
          },
          btn : {
            url : '#',
            text : 'read full article'
          } 
        },
        secondReview :{
          reviewer : 'mary maxey',
          journal : 'the guardian',
          stars :  '5',
          txt : {
            paragraph1 : 'Non arcu mauris tortor ultrices mollis tellus euismod fermentum. Habitant amet tincidunt id sapien accumsan sed.',
            paragraph2 : ''
            },
          btn : {
            url : '#',
            text : 'read full article'
          } 
        },
        thirdReview :{
          reviewer : 'patrick monroe',
          journal : 'globe and mail',
          stars :  '5',
          txt : {
            paragraph1 : 'Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Nulla porttitor accumsan tincidunt.',
            paragraph2 : ''
            },
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
@import '../../assets/style/variables.scss';
    .col-6{
      padding: 0;
    }
    .img-container{
        height: 700px;
        img{
            width: 100%;
            height: 100%;
        }
    }
    .card-container{
      background-color: $blackBg;
    }
</style>