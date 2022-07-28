<template>
  <div>
      <HeaderApp />
      <MainApp />
      <FooterApp />
  </div>
</template>

<script>
import HeaderApp from './components/HeaderApp.vue'
import MainApp from './components/MainApp.vue'
import FooterApp from './components/FooterApp.vue'

export default {
  name: 'App',
  components: {
    HeaderApp,
    MainApp,
    FooterApp,
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "./assets/style/variables.scss";
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Ibarra+Real+Nova:ital,wght@0,400;0,500;1,400&display=swap');
body{
font-family: 'Open Sans', sans-serif;
}
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.my-btn-white,
.my-btn-dark{
  width: 230px;
  font-size: 1rem;
  text-align: center;
  padding: 10px 0;
  cursor: pointer;
  font-family: 'Poppins', sans-serif;
  text-transform: uppercase;
  transition: all 0.5s ease-in;
}
.my-btn-white{
  border: 1px solid white;
  a{
      text-decoration: none;
      color: $txtColorWhite;
    }
     &:hover{
      background-color: white;
      border: 1px solid black;
      color: black;
  }
  &:hover a{
    color: black;
  }
}
.my-btn-dark{
  border: 1px solid $txtColorUnselected;
  margin: 0 auto;
  a{
    text-decoration: none;
    color: $blackBg;
  }
  &:hover{
      border: 1px solid black;
  }
}
.my-margin{
  margin-top: 130px;
}
</style>
