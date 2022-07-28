<template>
  <footer>
    <section>
      <div class="container-hero-footer">
          <div class="container-info-footer mx-auto pt-5">
              <div class="logo-container text-center mt-5">
                  <img src="/img/logo-restaurant-2x.png" alt="logo">
              </div>
              <div class="mt-5 text-center">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque pariatur tempore sint consequatur recusandae veniam enim nemo mollitia. Nihil, possimus consectetur.</p>
              </div>
              <div class="container-social d-flex justify-content-center mt-5">
                  <div class="social-ico align-items-center d-flex justify-content-center" v-for="(social , index) in socials" :key="index" :class="{'me-3' : index< (socials.length-1)}">
                      <a :href="social.url"><i :class="social.class"></i></a>
                  </div>
              </div>
          </div>
      </div>
    </section>
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
      socials : [
      {
        social : 'facebook',
        class : 'fa-brands fa-facebook-f',
        url : '#',
      },
      {
        social : 'twitter',
        class : 'fa-brands fa-twitter',
        url : '#',
      },
      {
        social : 'youtube',
        class : 'fa-brands fa-youtube',
        url : '#',
      },
      {
        social : 'instagram',
        class : 'fa-brands fa-instagram',
        url : '#', 
      },
      {
        social : 'linkedin',
        class : 'fa-brands fa-linkedin-in',
        url : '#', 
      },
      ],
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';
.container-hero-footer{
  width: 100%;
  height: 520px;
  background-image: url('../../public/img/footer2x.jpg');
  background-size: cover;
  background-position: center;
  color: $txtColorWhite;
  .container-info-footer{
    width: 500px;
      img{
        width: 300px;
      }
      p{
        text-shadow: 3px 3px 3px rgb(68, 68, 68);
      }
    .social-ico{
      background-color: $txtColorWhite;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      transition: all 0.5s ease-in;
      cursor: pointer;
      a{
        text-decoration: none;
        color: $blackBg;
      }
      &:hover{
        transform: scale(1.1);
      }
    }
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