<template>
  <div class="hero-container position-relative">
    <NavbarApp />
    <img src="/img/slider52x.jpg" alt="hero image">
    <div class="black-filter"></div>
    <OverlayDiscount />
  </div>
</template>

<script>
import NavbarApp from './NavbarApp.vue'
import OverlayDiscount from './OverlayDiscount.vue'
export default {
    components : {
        NavbarApp,
        OverlayDiscount,
    }
}
</script>

<style lang='scss' scoped>
.hero-container{
    height: 961px;
    img{
        width: 100%;
        height: 961px ;
        object-fit: cover;
        object-position: center;
    }
    .black-filter{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: linear-gradient( rgba(0, 0, 0, 0.4), transparent)
    }
}
</style>