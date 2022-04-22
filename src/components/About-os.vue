<template>
    <div class="wrapper">
        <div class="banner" :style="`background-image: url(${img}) ` ">

        </div>
        <!--  -->
        <div class="content">
            <h1>{{ title }}</h1>
            <p>{{ text }}</p>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            img: 'https://i.pinimg.com/236x/00/28/29/002829964f096fa148c44de307d27e03.jpg',
            title: 'Hello Title',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam cupiditate distinctio nemo voluptatem, repellendus itaque ratione beatae alias velit explicabo possimus quidem placeat dicta quo obcaecati dolorem fuga. Voluptatibus voluptas doloribus nisi aliquid sint dolore consequatur dolorem quam sunt, nam eos corporis corrupti temporibus obcaecati rem expedita officiis. Dignissimos, cumque.'
        }
    },
}
</script>

 <style lang="scss" scoped>
    .wrapper{
            display: flex;
            justify-content: space-between;
            align-items: center;
            .banner,
            .content{
                width: 47%;

            }
            .banner{
                
                min-height: 400px;
                background-position: center;
                background-size: cover;
                background-repeat: no-repeat;
             

            }
    }
</style>

