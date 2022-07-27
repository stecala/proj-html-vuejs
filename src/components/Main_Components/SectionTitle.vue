<template>
<div class="text-center my-margin">
    <h2 class="mb-4">
        {{txtTitle}}
    </h2>
    <SmallLine />
</div>
</template>

<script>
import SmallLine from './SmallLine.vue'
export default {
    components:{
        SmallLine,
    },
    props : {
        txtTitle: String
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/variables.scss';

    h2{
        font-family: 'Times New Roman', Times, serif;
        font-size: 3rem;
    }
</style>