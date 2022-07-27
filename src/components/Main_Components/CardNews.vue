<template>
  <div class="card-container position-relative">
    <div class="gradient-filter position-absolute d-flex align-items-center justify-content-center">
        <div class="text-center">
            <h4><i class="fa-solid fa-link"></i></h4>
            <p class="text-uppercase mt-4">{{element.title}}</p>
            <div>News</div>
        </div>
    </div>
    <div class="img-container position-absolute">
        <img :src="element.url" :alt="element.alt">
    </div>
    <div class="info-container text-center pt-5">
        <h3 class="text-uppercase">{{element.title}}</h3>
        <div class="sub-txt">
            <ul>
                <li>{{element.sub_text.author}}</li>
                <li class="divider">{{element.sub_text.date}}</li>
                <li>{{element.sub_text.categories}}</li>
            </ul> 
        </div>
    </div>
  </div>
</template>

<script>
export default {
    props :{
        element : Object,
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/variables.scss';
.card-container{
    width: calc(100% / 3 - 40px);
    height: 690px;
    .gradient-filter{
        top: 0;    
        left: 0;
        background-image: linear-gradient( rgba(0, 0, 0, 0.733), rgba(0, 0, 0, 0));
        width: 100%;
        height: 100%;
        z-index: 3;
        opacity: 0;
        transition : opacity 0.7s ease-in;
        color: $txtColorWhite;
        div{
            h4{
                cursor: pointer;
            }
            p{
                font-weight: 600;
                text-shadow: 2px 2px 2px black;
                font-family: 'Poppins', sans-serif;
            }
        }
    }
    .img-container{
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .info-container{
        width: 100%;
        position: absolute;
        bottom: 0;
        left: 0;
        background-color: $txtColorWhite;
        z-index: 2;
        opacity: 1;
        h3{
            font-size: 1.2rem;
            font-weight: 700;
            font-family: 'Poppins', sans-serif;
        }
        .sub-txt{
            color: $txtGrey;
            font-size: 0.7rem;
            ul{
                list-style: none;
                padding: 0;
                li{
                    display: inline-block;
                    padding: 7px;
                    position: relative;
                }
            }
        }
        .divider:before{
            content : "";
            position: absolute;
            left    : 0;
            top : 8px;
            width : 1px;
            height : 50%;
            background-color: $txtGrey;
        }
        .divider:after {
            content : "";
            position: absolute;
            right    : 0;
            top : 7px;
            width : 1px;
            height : 50%;
            background-color: $txtGrey;
        }
    }
    &:hover .info-container{
        animation: growth 0.7s;
        opacity: 0;
    }
    &:hover .gradient-filter{
            opacity: 1;
        }
    .growth{
        -webkit-animation: scale-out-ver-bottom 0.5s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
        animation: scale-out-ver-bottom 0.5s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
    }
    @-webkit-keyframes growth {
    0% {
        -webkit-transform: scaleY(1);
                transform: scaleY(1);
        -webkit-transform-origin: 0% 100%;
                transform-origin: 0% 100%;
        opacity: 1;
    }
    100% {
        -webkit-transform: scaleY(0);
                transform: scaleY(0);
        -webkit-transform-origin: 0% 100%;
                transform-origin: 0% 100%;
        opacity: 1;
    }
    }
    @keyframes growth {
    0% {
        -webkit-transform: scaleY(1);
                transform: scaleY(1);
        -webkit-transform-origin: 0% 100%;
                transform-origin: 0% 100%;
        opacity: 1;
    }
    100% {
        -webkit-transform: scaleY(0);
                transform: scaleY(0);
        -webkit-transform-origin: 0% 100%;
                transform-origin: 0% 100%;
        opacity: 1;
    }
    }   

}
</style>