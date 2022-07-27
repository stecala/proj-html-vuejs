<template>
  <div class="banner-container d-flex my-margin">
        <div class="img-container">
            <img :src="imgBanner" alt="Banner Img">
        </div>
        <div class="card-container">
            <div class="d-flex align-items-center align-cont">
                <CardForBanner :txtForCard="txtForCard" />
            </div>
        </div>
  </div>
</template>


<script>
import CardForBanner from '../CardForBanner.vue'
export default {
    props:{
        imgBanner : String,
    },
    components : {
        CardForBanner,
    },
    data : function(){
    return{
      txtForCard : {
          subtitle : 'fine dining experience',
          title : 'the best table in town',
          text : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga adipisci aut consequatur nam! Eius quas labore aperiam non.',
          btn : {
            url : '#',
            text_btn : 'explore the menu' 
          }
      },
    }
  }
}
</script>
<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

    .banner-container{
        width: 100%;
        max-height: 850px;
        overflow: hidden;
        .img-container{
            width: 60%;
            img{
                max-width: 100%;
                object-fit: cover;
                object-position: center;
            }
        }
        .card-container{
            width: 40%;        
            background-color: $blackBg;
            .align-cont{
                width: 100%;
                height: 100%;
                padding: 0 80px;
            }
        }
    }
</style>