<template>
  <div class="review-container">
    <div class="reviewer text-uppercase">{{element.reviewer}}</div>
    <div class="journal mt-4 text-uppercase">{{element.journal}}</div>
    <div v-for=" number in element.stars" :key="number" class="d-inline-block mt-4 me-2"><i class="fa-solid fa-star"></i></div>
    <div class="line mt-4"></div>
    <div class="txt mt-4">{{element.txt.paragraph1}}<br>
        <div class="spacer"></div>
        <span v-if="(element.txt.paragraph2 !='')">{{element.txt.paragraph2}}</span>
    </div>
    <BtnApp :element="element.btn.text" :elementURL="element.btn.url" :isWhite="isWhite" />
  </div>
</template>

<script>
import BtnApp from '../Common/BtnApp.vue'
export default {
    data: function(){
        return{
            isWhite : true,
        }
    },
    components :{
        BtnApp,
    },
    props : {
        element : Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';

    .review-container{
        padding: 0 120px;   
        color: $txtColorWhite;
        font-family: 'Bebas Neue', cursive;
        .reviewer{
            font-size: 1rem;
            font-family: 'Poppins', sans-serif;
        }
        .journal{
            font-size: 3.5rem;
            line-height: 1.2;
        }
        .line{
            width: 70px;
            height: 1px;
            background-color: $txtColorUnselected;
        }
        .txt{
            padding-right: 20px;
            font-size: 1.2rem;
            font-family: 'Ibarra Real Nova', serif;
            .spacer{
                width: 100%;
                height: 10px;
            }
        }
      
    }
</style>