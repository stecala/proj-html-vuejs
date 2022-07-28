<template>
    <div class="mt-5 my-btn-white" :class="isWhite ? 'my-btn-white' : 'my-btn-dark'">
        <a :href="elementURL">{{element}}</a>
    </div>
</template>

<script>
export default {
    props: {
        isWhite : Boolean,
        element : String,
        elementURL : String,
    }
}
</script>

<style>

</style>