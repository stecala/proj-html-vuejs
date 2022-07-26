<template>
  <header>
    <div class="container-fluid">
      <div class="row">
        <div class="col-4">
            <HeroDescription />
        </div>
        <div class="col-8">
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
  .col-4, 
  .col-8{
    padding: 0;
  }

}
</style>
