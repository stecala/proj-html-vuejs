<template>
  <main class="mt-5">
      <PromoComponent />
  </main>
</template>

<script>
import PromoComponent from './Main_Components/PromoComponent.vue'
export default {
  components :{
    PromoComponent,
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';
  img{
    width: 100%;
  }
  .roll-name{
    color: $txtColorWhite;
    bottom: 15px;
    left: 35%;
    font-weight: bold;
  }

</style>