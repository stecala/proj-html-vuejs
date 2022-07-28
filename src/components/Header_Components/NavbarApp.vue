<template>
  <div class="position-absolute  w-100" id="navbar">
    <div class="row text-center pt-5 w-100 ">
        <div class="col-12 d-flex mx-auto justify-content-around flex-wrap w-100">
            <div class="d-flex " v-for="(element, index) in nav" :key="index" :class="element.selected == false ? 'unselected' : 'selected'">
                <div >
                <a :href="element.url">{{element.name}}</a> 
                </div>
                <div class="new ms-2 align-self-center" v-if="element.new">
                    <span>NEW</span>
                </div>
            </div>
            <div class="unselected">
                <i class="fa-solid fa-cart-shopping"></i>
            </div>
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
                    url : '#menu',
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
#navbar{
    a{
        text-decoration: none;
    }
}
.position-absolute{
    top: 0;
    left: 0;
    font-weight: 300;
}
.selected{
    a{
        color : $txtColorWhite;
    }
}
.unselected{
    a{
        color: $txtColorUnselected;
    }
    &:hover a{
        color: $txtColorWhite;
    }
}
.row{
    font-size: 1rem;
    font-weight: 500;
    div{
        width: fit-content;
        z-index: 1;
        cursor: pointer;
        .new{
            color: $txtColorWhite;
            font-size: 0.6rem;
            font-weight: bold;
            border: 1px solid $txtColorUnselected;
            padding: 2px 7px;
        }
    }
}

</style>