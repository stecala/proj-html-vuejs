<template>
<div>
    <h2>
        ciao ciao
    </h2>
    <SmallLine />
</div>
</template>

<script>
import SmallLine from './SmallLine.vue'
export default {
    components:{
        SmallLine,
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/variables.scss';

    h2{
        font-family: 'Times New Roman', Times, serif;
        font-style: italic;
    }
</style>