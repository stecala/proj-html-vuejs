<template>
<div>
    <section>
        <div class="my-margin d-flex justify-content-center ">

                
                <div class="single-menu position-relative " v-for="menu in menus" :key="menu.id" @click="setCurrentId(menu.id)" :class="(menu.id==currentID) ? 'selected-menu' : 'unselected-menu' " >
                    <a href="#section">
                        <div class="img-cont" v-if="menu.id==currentID">
                            <img :src="menu.menu_img" alt="menu image">
                        </div>
                        <div class="gradient-bg position-absolute" v-if="menu.id==currentID"></div>

                        <div class="highlight px-5 pt-5">
                            <h2 class="mt-5 ms-5">{{menu.title}}</h2>
                            <div class="single-section-menu mt-5 px-5" v-for="dish in menu.dishes" :key="dish.id">
                                <div class="row align-items-center">
                                    <div class="col-10">
                                        <span class="title-dish">{{dish.dish}}</span>
                                    </div>
                                    <div class="col-2">
                                        <span>{{dish.price}}</span>
                                    </div>
                                    <div class="col-12 pt-4">
                                        <span>{{dish.description}}</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </a>
                
                </div>
        </div>
    </section>
    <section>
        <div class="banner-section my-margin position-relative d-flex align-items-center " id="section">
            

            <div class="position-absolute img-banner">
                    <img :src="menus[currentID].banner_img" alt="banner img">
            </div>

            <div class="card-container position-relative" >

                <div class="slider-left position-absolute" @click="goPrevDish()">
                    <i class="fa-solid fa-angle-left"></i>
                </div>

                <div class="slider-right position-absolute" @click="goNextDish()">
                    <i class="fa-solid fa-angle-right"></i>
                </div>

                <div class="row">
                    <div class="col-9">
                        <h2 class="text-uppercase card-title">
                            {{menus[currentID].dishes[dishesID].dish}}
                        </h2>
                    </div>
                    <div class="col-3 text-end fw-semibold pt-3 ">
                        <span>{{menus[currentID].dishes[dishesID].price}}</span>
                    </div>
                </div>
                <div class="row px-3">
                    <div class=" col-12 p-0">
                        <div class="divider"></div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12 mt-5">
                        <span>{{menus[currentID].dishes[dishesID].description}}</span>
                    </div>
                </div>
            </div>

        </div>
    </section>
</div>
</template>

<script>
export default {
    data : function(){
        return{
            menus : [
                {
                    id : '0',
                    title : "hors d'oeuvres",
                    'menu_img' : '/img/menu-hors.jpg',
                    'banner_img' : "/img/Hors-d’oeuvre.jpg",
                    dishes : [
                        {
                            id : 0,
                            dish : 'ahi salmon nighiri',
                            price : '$48',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 1,
                            dish : 'umi masu salad',
                            price : '$21',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 2,
                            dish : 'temaki with crab',
                            price : '$32',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 3,
                            dish : 'california rolls',
                            price : '$22',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                    ]   
                },
                {
                    id : '1',
                    title : 'main course',
                    'menu_img' : '/img/misc22x.jpg',
                    'banner_img' : "/img/hero42x.jpg",
                    dishes : [
                        {
                            id : 0,
                            dish : 'braised abalone',
                            price : '$52',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 1,
                            dish : 'twice cooked pork',
                            price : '$21',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 2,
                            dish : 'kung pao chicken',
                            price : '$32',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 3,
                            dish : 'char siu & sushis',
                            price : '$48',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                    ]   
                },
                {
                    id : '2',
                    title : 'desserts',
                    'menu_img' : '/img/vertical-dessertjpg.jpg',
                    'banner_img' : "/img/fancy-desserts.jpg",
                    dishes : [
                        {
                            id : 0,
                            dish : 'chocolate ball cake',
                            price : '$13',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 1,
                            dish : 'lime pie with crust',
                            price : '$14',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 2,
                            dish : 'rasberry pear cake',
                            price : '$18',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                        {
                            id : 3,
                            dish : 'café au lait',
                            price : '$6',
                            description : 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
                        },
                    ]   
                },
            
            ],
            currentID : 1,
            dishesID : 0,
        }
    },
    methods :{
        setCurrentId(elementID){
            this.currentID = elementID
            this.dishesID = 0
        },
        goNextDish(){
            this.dishesID = this.dishesID +1
            if(this.dishesID == this.menus[this.currentID].dishes.length){
                this.dishesID = 0
            }
        },
        goPrevDish(){
            this.dishesID = this.dishesID - 1
            if(this.dishesID == - 1){
                this.dishesID = this.menus[this.currentID].dishes.length - 1
            }
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';
.single-menu{
    width: calc(100% / 3 - 100px);
    background-color: $bgGrey;
    min-height: 850px;
    cursor: pointer;
    transition: all 0.5s;
    .img-cont{
        width: 100%;
        height: 100%;
        img{
            width: 100%;
            height: 860px;
            object-fit: cover;
            object-position: center;
        }
    }
    .highlight{
        position: absolute;
        top: 0;
        left: 0;
        z-index: 3;
    }
    .gradient-bg{
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: linear-gradient( rgb(0, 0, 0), rgba(0, 0, 0, 0.452));
        z-index: 2;
    }
    h2{
        text-transform: uppercase;
        font-size: 2rem;
        font-weight: 700;
        line-height: 1.2;
    }
    .single-section-menu{
        .title-dish{
            text-transform: uppercase;
            font-size: 1.3rem;
            font-weight: 700;
        }
    }
}
.unselected-menu{
    a{
        color: $blackBg;
    }
}
.selected-menu{
    a{
        color: $txtColorWhite;
    }
        transform: translateY(-50px);
    
}
.banner-section{
    width: 100%;
    min-height: 800px;
    .img-banner{
        top: 0;
        left: 0;
        width: 100%;
        z-index: -1;
        img{
            width: 100%;
            height: 800px;
            object-fit: cover;
            object-position: center;
        }
    }
    .card-container{
        width: 530px;
        min-height: 600px;
        margin-left: 300px;
        background-color: $blackBg;
        color: $txtColorWhite;
        padding: 90px;

        .slider-left{
            left: 6px;

        }
        .slider-right{
            right: 6px;        
        }

        .slider-left,
        .slider-right{
            top: 45%;
            font-size: 2rem;
        }


        .card-title{
            font-size: 3rem;
            font-weight: 700;
            line-height: 1.4;
        }
        .divider{
            width: 60px;
            height: 1px;
            background-color: $txtColorUnselected;
            margin-top: 70px;
        }
    }
    
}
</style>