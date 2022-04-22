<template >
  <div class="container">
     <div class="wrapp">
        <button-nav-vue @action="setIndex" />
       <!-- INFO -->
        <component :is="activeComp[activIndex]" @setModal="setModal"></component>
        <Modal :v-if="isOpen" :image="modalImage"/>
     </div>
  </div>
</template>


<script>
import ButtonNavVue from './components/Button-nav.vue'
import Aboutos from './components/About-os.vue'
import Team from './components/Team.vue'
import Cerd from './components/Cerd.vue'
import Modal from './components/Modal.vue'
export default {
  
  components:{
    ButtonNavVue,
    Aboutos,
    Team,
    Cerd,
    Modal

  },

  data() {
    return {
      isOpen:false,
      modalImage : '',
      activIndex :0,
      activeComp :[
        'Aboutos',
        'Team',
        'Cerd'
      ],
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

  methods: {
    setIndex(idx) {
      this.activIndex = idx
    }
  },
  setModal(img) {
      this.modalImage = img
      this.isOpen = true  
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
  h1::selection{
    background: red;
    color: aqua;
  }
</style>