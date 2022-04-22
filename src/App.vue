<template >
  <div class="container">
     <div class="wrapp">
        <button-nav-vue />
        <h1>{{ activIndex }}</h1>
     </div>
  </div>
</template>


<script>
import ButtonNavVue from './components/Button-nav.vue'
export default {
  components:{
    ButtonNavVue

  },

  data() {
    return {
      activIndex :0,
      aboutData: [
        {
          btnName: 'About us'
        },

            {
          btnName: 'Our team'
        },


            {
          btnName: 'Certificates'
        }


      ]
    }
  },

  provide() {
    return {
      btnInfo : this.aboutData
    }
  }

}
</script>



<style lang="scss">
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .container{
    width: 1110px;
    margin: 0 auto;
  }
  button{
    outline: none;
    cursor: pointer;
    background: none;
  }
  body{
    font-family: 'Gill Sans',sans-serif;
    color: #333;
    font-size: 15px;
    // background: #fff;
    background:linear-gradient(to right,#040016,#060020,#090030);
  }
</style>