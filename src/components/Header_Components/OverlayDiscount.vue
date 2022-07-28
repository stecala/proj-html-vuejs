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
            <div class="col-12 single-icon text-center d-flex flex-column justify-content-between align-items-center pb-2 pt-3">
                <div>
                    <p class="position-relative">39</p>
                </div>
                 <div> 
                    <span>On Sale</span>
                </div>
            </div>
        </div>
  </div>
</template>

<script>
export default {

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
    
</style>
 