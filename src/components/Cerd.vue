<template>
    <div class="wrapper">
        <div class="cert">
            <img  
            v-for="cert in certs" 
            :key="cert" 
            :src="cert" alt=""
            @click="$emit(`setModal`, cerd)"
            >
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            certs: [
                'https://i.pinimg.com/236x/3a/1c/f5/3a1cf58dda78eebdeb6a14f59767b885.jpg',
                'https://i.pinimg.com/236x/c0/76/4d/c0764d74c4d4402bf0b68febb8808130.jpg',
                'https://i.pinimg.com/236x/bc/84/ab/bc84ab54a32333a2d50840049aa63b47.jpg',
                'https://i.pinimg.com/236x/23/e1/c4/23e1c46b843032387b9c95392e017979.jpg'
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
    .cert{
        display: flex;
        justify-content: space-between;
        img{
            width: 250px;
            height: 300px;
            object-fit: cover;
            cursor: pointer;
        }
    }
</style>