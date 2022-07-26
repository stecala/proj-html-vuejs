<template>
  <header>
    <div class="container-fluid">
      <div class="row">
        <div class="my-col-small">
            <HeroDescription :txtForCard="txtForCard" />
        </div>
        <div class="my-col-big">
            <HeroImg /> 
        </div> 
      </div>
    </div>
  </header>
</template>

<script>
import HeroDescription from './Header_Components/HeroDescription.vue'
import HeroImg from './Header_Components/HeroImg.vue'

export default {
  components :{
    HeroDescription,
    HeroImg,
  },
  data : function(){
    return{
      txtForCard : {
          subtitle : 'the best table in town',
          title : 'fine dining experience',
          text : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga adipisci aut consequatur nam! Eius quas labore aperiam non.',
          btn : {
            url : '#',
            text_btn : 'explore the menu' 
          }
      }
    }
  }
}
</script>

<style scoped lang="scss">
header{
.my-col-small{
  width: 40.7%;
}
.my-col-big{
  width: 59.3%;
}
.my-col-small,
.my-col-big{
  padding: 0;
}
}
</style>
