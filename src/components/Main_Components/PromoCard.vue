<template>
  <div class="col-4 text-center px-5">
        <div class="mb-5">
            <img :src="element.img" alt="sushi">
        </div>
        <h2>{{element.title}}</h2>
        <div class="small-line"></div>
        <p>
            {{element.txt}}
        </p>
        <div class="my-btn-dark mt-4 mx-auto">
            <a :href="element.btn.url">{{element.btn.txt_btn}}</a>
        </div>
  </div>
</template>

<script>
export default {
    props :{
        element : Object
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/variables.scss';
h2{
    font-size: 2rem;
    font-family: 'Bebas Neue', cursive;

}
.small-line{
    width: 40px;
    height: 1px;
    background-color: $txtColorUnselected;
    margin: 10px auto;
}

</style>