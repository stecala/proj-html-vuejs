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
import CardForBanner from '../Common/CardForBanner.vue'
export default {
    props:{
        imgBanner : String,
        txtForCard : Object,
    },
    components : {
        CardForBanner,
    },
}
</script>
<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

    .banner-container{
        width: 100%;
        max-height: 850px;
        .img-container{
            width: 60%;
            height: 100%;
            img{
                width: 100%;
                height: 850px;
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