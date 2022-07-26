<template>
  <div class="position-absolute">
    <div class="row text-center pt-5 ">
        <div class="px-4" v-for="(element, index) in nav" :key="index" :class="{unselected : element.selected == false}">
            {{element.name}}
        </div>
        <div class="unselected">
            <i class="fa-solid fa-cart-shopping"></i>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    data : function (){
        return{
            nav : [
                {
                    name : 'Home',
                    url : '#',
                    new : false,
                    selected : true,
                },
                {
                    name : 'Culinary History',
                    url : '#',
                    new : false,
                    selected : false,
                },
                {
                    name : 'Our Team',
                    url : '#',
                    new : false,
                    selected : false,
                },
                {
                    name : 'Our Menu',
                    url : '#',
                    new : false,
                    selected : false,
                },
                {
                    name : 'Takeout',
                    url : '#',
                    new : true,
                    selected : false,
                },
                {
                    name : 'Bulletin',
                    url : '#',
                    new : false,
                    selected : false,
                },
                {
                    name : 'Reservation',
                    url : '#',
                    new : false,
                    selected : false,
                },
            ],
        
        }
    },
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';
.position-absolute{
    color : $txtColorWhite;
    top: 0;
    left: 8%;
    font-weight: 300;
}
.unselected{
 color: $txtColorUnselected;
}
.row{
    font-size: 1rem;
    font-weight: 500;
    div{
        width: fit-content;
        display: inline-block;
        z-index: 1;
        cursor: pointer;
    }
}
</style>