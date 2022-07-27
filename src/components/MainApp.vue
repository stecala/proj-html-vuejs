<template>
  <main class="mt-5">
      <PromoComponent />
      <PromoCardsList :cardsList="cardsList" />
      <BannerMain :imgBanner="imgBanner[0]" />
      <SectionTitle :txtTitle="txtTitle[0]" />
      <ReviewSection />
  </main>
</template>

<script>
import PromoComponent from './Main_Components/PromoComponent.vue'
import PromoCardsList from './Main_Components/PromoCardsList.vue'
import BannerMain from './Main_Components/BannerMain.vue'
import SectionTitle from './Main_Components/SectionTitle.vue'
import ReviewSection from './Main_Components/ReviewSection.vue'
export default {
  components :{
    PromoComponent,
    PromoCardsList,
    BannerMain,
    SectionTitle,
    ReviewSection,
  }, 
  data : function(){
    return{
      cardsList : [
        {
          img : '/img/sushi-1.png',
          title : 'the best table in town',
          txt : 'Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi tortor id gravida aliquet.',
          btn : {
            url : '#',
            'txt_btn': 'explore the menu',
          }
        },
         {
          img : '/img/sushi-2.png',
          title : 'perfect for groups',
          txt : 'Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi tortor id gravida aliquet.',
          btn : {
            url : '#',
            'txt_btn': 'make a reservation',
          }
        },
         {
          img : '/img/sushi-3.png',
          title : 'fresh produce everyday',
          txt : 'Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi tortor id gravida aliquet.',
          btn : {
            url : '#',
            'txt_btn': 'learn more about us',
          }
        },
      ],
      imgBanner : ['/img/slider32x.jpg' , '/img/slider72x-scaled.jpg'],
      txtTitle : ['What critics are saying about us', 'Latest news & promotions'],
    }
  },
}
</script>

<style lang="scss" scoped>


</style>