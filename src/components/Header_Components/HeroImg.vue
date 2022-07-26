<template>
  <div class="hero-container">
    <NavbarApp />
    <img src="../../../public/img/slider52x.jpg" alt="hero image">
  </div>
</template>

<script>
import NavbarApp from './NavbarApp.vue'
export default {
    components : {
        NavbarApp,
    }
}
</script>

<style lang='scss' scoped>
.hero-container{
    height: 100vh;
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center;
    }
}
</style>