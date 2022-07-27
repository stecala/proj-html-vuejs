<template>
  <div class="container-lg mt-5 pt-3">
    <div class="row">
      <div class="col-6 img-container">
          <img src="/img/blog72x-1200x1375.jpg" alt="Girl cooking">
      </div>
      <div class="col-6 text-zone d-flex align-items-center card-container justify-content-center my-hover">
          <ReviewCard :element="textCardsReview.firstReview" />
      </div>
    </div>
    <div class="row mt-5">
       <div class="my-col me-5 my-hover">
            <ImgGradient :element="textCardsReview.secondReview" :imgSrc="imgSrc[0]" />
       </div>
       <div class="my-col my-hover" >
            <ImgGradient :imgSrc="imgSrc[1]" :element="textCardsReview.thirdReview" />
       </div>
    </div>
  </div>
</template>

<script>
import ReviewCard from './ReviewCard.vue'
import ImgGradient from './ImgGradient.vue'
export default {
  components : {
    ReviewCard,
    ImgGradient
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
          stars :  5,
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
          stars :  5,
          txt : {
            paragraph1 : 'Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus. Nulla porttitor accumsan tincidunt.',
            paragraph2 : ''
            },
          btn : {
            url : '#',
            text : 'read full article'
          } 
        },
      },
      imgSrc : ['/img/info52x.jpg' , '/img/info12x.jpg' ],
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
    .my-col{
      width: calc((100% / 2) - 1.5rem);
      padding: 0;
    }
    .my-hover{
      transition: transform 0.5s ease-in;
      &:hover{
              cursor: pointer;
              transform: scale(1.05);
          } 
    }
</style>