<template>
  <div class="wrapper">
      <div class="card" v-for="member in team" :key="member.name">
          <img :src="member.img" alt="">
          <h3>{{ member.name }}</h3>
          <p> {{ member.job }} </p>
      </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
           team:[
               {
                 img: 'https://i.pinimg.com/236x/be/22/63/be226396678f3729c9ecdba2a2d1d3f1.jpg' ,
                 name: 'Lassetti 1.8',
                 job: 'GM Uzbekistan' 
               },
                       {
                 img: 'https://i.pinimg.com/236x/e7/ed/05/e7ed0566ff4fd325347cc953e30feb23.jpg' ,
                 name: 'Gentra 1.5',
                 job: 'GM Uzbekistan' 
               },
                       {
                 img: 'https://i.pinimg.com/236x/86/1d/dc/861ddcb7ec605bf724eb187f5e88c303.jpg' ,
                 name: 'LADA vesta',
                 job: 'Rossiya Lada' 
               },

                        {
                 img: 'https://i.pinimg.com/236x/86/1d/dc/861ddcb7ec605bf724eb187f5e88c303.jpg' ,
                 name: 'LADA vesta',
                 job: 'Rossiya Lada' 
               }
           ] 
        }
    },
}
</script>

<style lang="scss"  scoped>
    .wrapper{
        display: flex;
        justify-content: space-between;

        .card{
            width: 250px;
            img{
                width: 100%;
                height: 300px;
                object-fit: cover;
            }
            h3{
                font-size: 30px;
                margin:15px 0;
            }
            p{
                color: aqua;
            }
        }
    }
</style>