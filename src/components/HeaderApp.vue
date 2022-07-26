<template>
  <header>
      <HeroDescription />
      <HeroImg />
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
  min-height: 100vh;
}
</style>
