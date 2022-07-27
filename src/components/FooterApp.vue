<template>
  <footer>
    <div class="container-hero-footer">
        <img src="/img/footer2x.jpg" alt="bar">
    </div>
    <div class="credits py-4 text-center">
        <ul>
            <li v-for="(credit, index) in creditsList" :key="index">
              {{credit}}
            </li>
        </ul>
    </div>
  </footer>
</template>

<script>
export default {
  data : function(){
    return{
      creditsList : ['Copyright 2012 - 2019 Avada' , 'All Right Reserved', 'Powered by Stefano 🐸' , 'ThemeFusion'],
    }
  }
}
</script>

<style lang="scss">
@import '../assets/style/variables.scss';
.container-hero-footer{
  width: 100%;
  height: 520px;
  overflow: hidden;
  img{
    width: 100%;
    height: 600px;
    object-fit: cover;
    object-position: bottom;
  }
}
.credits{
  background-color: $blackBg;
  color: $txtColorUnselected;
  font-size: 0.8rem;
  ul{
    list-style: none;
    padding: 0;
    li{
      display: inline-block;
      padding: 0 10px;
    }
  }
}
</style>