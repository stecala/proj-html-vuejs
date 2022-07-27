<template>
  <main class="mt-5">
    <section>
      <PromoComponent />
      <PromoCardsList :cardsList="cardsListPromo" />
    </section>
    
    <section>
      <BannerMain :imgBanner="imgBanner[0]" />
    </section>
    
    <section>
      <SectionTitle :txtTitle="txtTitle[0]" />
      <ReviewSection />
    </section>
   
    <section class="jumbotron position-relative my-margin">
      <img src="/img/page52x.jpg" alt="kung pao chicken">
      <div class="position-absolute txt-jumbo text-uppercase text-center">kungo pao chicken - $32</div>
    </section>

    <section>
      <SectionTitle :txtTitle="txtTitle[1]" />
      <div class="card-news-container container-lg mt-5 d-flex justify-content-between">
          <CardNews v-for="(element, index) in cardsListNews" :key="index" :element="element" />
      </div>
    </section>
  </main>
</template>

<script>
import PromoComponent from './Main_Components/PromoComponent.vue'
import PromoCardsList from './Main_Components/PromoCardsList.vue'
import BannerMain from './Main_Components/BannerMain.vue'
import SectionTitle from './Main_Components/SectionTitle.vue'
import ReviewSection from './Main_Components/ReviewSection.vue'
import CardNews from './Main_Components/CardNews.vue'
export default {
  components :{
    PromoComponent,
    PromoCardsList,
    BannerMain,
    SectionTitle,
    ReviewSection,
    CardNews,
  }, 
  data : function(){
    return{
      cardsListPromo : [
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
      cardsListNews : [
      {
        url : '/img/blog92x-1200x1375.jpg',
        alt : 'coffee',
        title : 'the best coffee in town',
        'sub_text' : {
          author : 'By author',
          date : 'January 7th, 2020',
          categories : 'Categories: News'
        },
      },
      {
        url : '/img/blog72x-1200x1375.jpg',
        alt : 'coocking',
        title : 'discover our new menu',
        'sub_text' : {
          author : 'By author',
          date : 'January 7th, 2020',
          categories : 'Categories: News'
        },
      },
      {
        url : '/img/blog82x.jpg',
        alt : 'square payment',
        title : 'we now accept square!',
        'sub_text' : {
          author : 'By author',
          date : 'January 7th, 2020',
          categories : 'Categories: News'
        },
      },
      
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';
.jumbotron{
  width: 100%;
  height: 600px;
    img{
      width: 100%;
      height: 100%;
    }
    .txt-jumbo{
      left: 0;
      bottom: 15px;
      width: 100%;
      color : $txtColorWhite;
      font-size: 0.8rem;
      font-weight: bolder;
    }

}

</style>