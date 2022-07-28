<template>
  <div class="my-margin">
    <div class="single-menu mx-auto">
    </div>
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
                    'banner_img' : "/img/Hors-d'oeuvre.jpg",
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
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/variables.scss';
.single-menu{
    max-width: calc(100% / 3 - 200px);
}

</style>