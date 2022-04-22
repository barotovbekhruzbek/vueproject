<template>
    <div class="layer" @click="$emit(`closeModal`)">
        <img :src="image" alt="">
    </div>
</template>

<script>
export default {
    props: {
        image: String
    }
}
</script>

<style lang="scss">
    .layer{
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        min-height: 100vh;
        background: rgba($color: #000, $alpha: 0.8);
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: center;

        img{
            width: 70%;
        }
    }
    
</style>

