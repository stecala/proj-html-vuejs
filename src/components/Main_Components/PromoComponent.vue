<template>
  <div class="pt-5">
    <div class="container-lg my-margin">
        <div class="row">
            <div class="col-6">
                <div class="promo-text mt-5">
                <p>
                    <strong>HAC TELLUS, FELIS RISUS AT</strong> mattis mattis. Eget euismod semper eget tortor, donec amet, blandit. Tristique facilisi faucibus elementum feugiat in nam in feugiat. Ipsum odio etiam duis facilisis amet vulputate.
                </p>
                <h2 class="mt-5">FOOD IS OUR COMMON <br>GROUND, A UNIVERSAL <br>EXPERIENCE</h2>
                <p class="mt-5">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. In similique
                    sequi enim eligendi id quaerat. Quod doloremque magni temporibus,
                    voluptatum, ipsum voluptatem consequuntur labore inventore repellat
                    hic quisquam praesentium laboriosam!
                </p>
                <img src="../../../public/img/signature.jpg" alt="signature" class="mt-3"/>
            </div>
            
            </div>
            <div class="col-6 position-relative img-container">
                <img src="../../../public/img/info22x.jpg" alt="california roll">
                <div class="position-absolute roll-name">
                    <span class="text-uppercase">california rolls - $22</span>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';
.promo-text{
    width: 90%;
    p{
        font-size: 1.2rem;
    }
    h2 {
        font-size: 4rem;
        font-family: 'Bebas Neue', cursive;
    }
    img {
        margin-top: 25px;
        width: 150px;
    }
}
.img-container{
    height: 795px;
    overflow: hidden;
    padding: 0;
    transition: all 0.5s ease-in;
    img{
        width: 100%;
        object-fit: cover;
        object-position: center;
    }
    .roll-name{
        color: $txtColorWhite;
        bottom: 15px;
        left: 35%;
        font-weight: bold;
    }
    &:hover{
        box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.308);
        transform: scale(0.95);
        cursor: pointer;
    }
}
</style>