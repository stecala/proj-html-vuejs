<template>
  <main class="mt-5">
      <PromoComponent />
      <PromoList />
  </main>
</template>

<script>
import PromoComponent from './Main_Components/PromoComponent.vue'
import PromoList from './Main_Components/PromoList.vue'
export default {
  components :{
    PromoComponent,
    PromoList,
  }
}
</script>

<style lang="scss" scoped>


</style>