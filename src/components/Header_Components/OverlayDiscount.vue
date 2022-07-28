<template>
  <div class="discount-container " >
        <div class="row">
            <div class="col-12 single-icon text-center d-flex flex-column justify-content-between align-items-center pb-2 pt-3">
                <div>
                    <i class="fa-solid fa-folder-open"></i><br>
                </div>
                <div> 
                    <span>Demos</span>
                </div>
            </div>
        </div>
        <div class="row mt-2">
            <div class="col-12 single-icon text-center d-flex flex-column justify-content-between align-items-center pb-2 pt-3" @click="addToCart()"> 
                <div>
                    <p class="position-relative">39</p>
                </div>
                 <div> 
                    <span>On Sale</span>
                </div>
            </div>
        </div>
        <div class="row mt-4">
            <div class="col-12 pop-up-icon d-flex align-items-center position-relative" v-if="isActive" :class="{ 'slide-in-right' : isActive }">
                    <span>
                        <i class="fa-solid fa-cart-arrow-down"></i>
                    </span>
                    <div class="notification text-center">
                        <i class="fa-solid fa-plus"></i><i class="fa-solid fa-1"></i>
                    </div>
            </div>
        </div>
  </div>
</template>

<script>
export default {
    data : function(){
        return{
            isActive : false
        }
    },
    methods:{
        addToCart() {
            this.isActive = true
            setTimeout(() => {
                this.isActive = false
            },2000)
        },
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/variables.scss';
    .discount-container{
        position: fixed;
        top: 300px;
        right: 20px;
        color: $txtGrey;
        .single-icon{
            background-color: $txtColorWhite;
            border-radius: 10px;
            width: 80px;
            height: 80px;
            cursor: pointer;
            box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.671);
        }
    }
    span{
        font-size: 0.7rem;
        font-weight: 700;
    }
    i{
        font-size: 1.3rem;
    }
    p{
        font-size: 1.3rem;
        font-weight: 700;
        margin: 0;
        color: $greenTxt;
        &::before{
            content: '$';
            position: absolute;
            left: -10px;
            top: 0;
            font-size: 0.9rem;
        }
    }
    .pop-up-icon{
        background-color: $txtColorWhite;
        width: 50px;
        height: 50px;
        border-radius: 5px 5px 5px 5px;
        transition: all ease-in-out;
        box-shadow: 5px 5px 5px  rgba(0, 0, 0, 0.671);

    }
    .notification{
        position: absolute;
        top: -25%;
        right: -30%;
        width: 30px;
        height: 30px;
        background-color: red;
        color: white;
        border-radius: 50%;
        box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.671);

        i{
            font-weight: 700;
            font-size: 0.8rem;
        }
    }
   .slide-in-right {
	-webkit-animation: slide-in-right 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
	animation: slide-in-right 0.5s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
    }
    @-webkit-keyframes slide-in-right {
    0% {
        -webkit-transform: translateX(1000px);
                transform: translateX(1000px);
        opacity: 0;
    }
    100% {
        -webkit-transform: translateX(0);
                transform: translateX(0);
        opacity: 1;
    }
    }
    @keyframes slide-in-right {
    0% {
        -webkit-transform: translateX(1000px);
                transform: translateX(1000px);
        opacity: 0;
    }
    100% {
        -webkit-transform: translateX(0);
                transform: translateX(0);
        opacity: 1;
    }
    }
</style>
 