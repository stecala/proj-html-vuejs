<template>
  <header>
    <div class="container-fluid">
      <div class="row">
        <div class="my-col-small">
            <HeroDescription />
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
  padding: 0;
}
}
</style>
