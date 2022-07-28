<template>
  <div class="col-4 text-center px-5">
        <div class="mb-5">
            <img :src="element.img" alt="sushi">
        </div>
        <h2>{{element.title}}</h2>
        <SmallLine />
        <p>
            {{element.txt}}
        </p>
        <BtnApp :isWhite="isWhite" :element="element.btn.txt_btn" :elementURL="element.btn.url"/>
  
  </div>
</template>

<script>
import SmallLine from './SmallLine.vue'
import BtnApp from '../Common/BtnApp.vue'
export default {
    data : function(){
        return{
            isWhite : false,
        }
    },
    components:{
        SmallLine,
        BtnApp,
    },
    props :{
        element : Object
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/variables.scss';
h2{
    font-size: 2rem;
    font-family: 'Bebas Neue', cursive;

}


</style>