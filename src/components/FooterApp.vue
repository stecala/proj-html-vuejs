<template>
  <footer>
    <div class="container-hero-footer">
        <img src="/img/footer2x.jpg" alt="bar">
    </div>
    <section>
      <div class="credits py-4 text-center">
          <ul>
              <li v-for="(credit, index) in creditsList" :key="index" :class="{divider : index < (creditsList.length-1)}">
                {{credit}}
              </li>
          </ul>
      </div>
    </section>
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
  font-weight: bolder;
  ul{
    list-style: none;
    padding: 0;
    li{
      display: inline-block;
      padding: 0 10px;
    }
    .divider{
      position: relative;
    &:after {
            content : "";
            position: absolute;
            right    : 0;
            top : 2px;
            width : 1px;
            height : 70%;
            background-color: $txtGrey;
        }
    }
  }
}
</style>