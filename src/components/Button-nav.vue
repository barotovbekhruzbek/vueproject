<template>
  
    <div class="btn-block">
         <TheButtonVue  @action="setIndex" />
    </div>
 
</template>
<script>
import TheButtonVue from './The-button.vue'
export default {
    components:{
            TheButtonVue
    },
    methods: {
        setIndex (idx) {
            this.$emit('action',idx)
        }
    },
}
</script>
<style lang="scss">
    .btn-block{
        display: flex;
        justify-content: center;
        margin: 100px 0 120px;

    }
</style>