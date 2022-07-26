<template>
  <div class="container-lg mt-5">
     <div class="row">
        <PromoCard />
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