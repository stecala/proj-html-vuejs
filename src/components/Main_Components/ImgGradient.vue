<template>
  <div class="img-container position-relative">
    <img :src="imgSrc" alt="">
    <div class="black-filter"></div>
    <div class="position-absolute">
        <ReviewCard :element="element" />
    </div>
  </div>
</template>

<script>
import ReviewCard from './ReviewCard.vue'
export default {
    components:{
        ReviewCard,
    },
    props: {
        element: Object,
        imgSrc: String,
    }
}
</script>

<style lang="scss" scoped>
    .img-container{
        max-height: 680px;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
        .black-filter{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: linear-gradient( rgb(0, 0, 0), rgba(0, 0, 0, 0.349))
        }
        .position-absolute{
            top: 20%;
            left: 0;
        }
    }
</style>