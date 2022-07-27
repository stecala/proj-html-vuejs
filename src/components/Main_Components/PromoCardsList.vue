<template>
  <div class="container-lg my-5 pt-5">
     <div class="row">
        <PromoCard  v-for="(element , index) in cardsList" :key="index"  :element="element" />
     </div>
  </div>
</template>

<script>
import PromoCard from './PromoCard.vue'
export default {
  components :{
    PromoCard,
  },
  props: {
    cardsList : Array,
  }
}
</script>

<style>

</style>