<template>
  <HeaderTop pageTitle="UFC Men's Pound for Pound Rankings" rankDate="11/21/2022"></HeaderTop>
  <div class="container">
  
  <div class = "rankdata"><RankingBox :p4prankings="p4prankings" /></div>
  
  </div>
</template>

<script>
import HeaderTop from '../emilianovega_vue/HeaderTop.vue';
import RankingBox from '../emilianovega_vue/RankingBox.vue';

export default {
  name: 'App',
  components: {
    HeaderTop,
    RankingBox
  },

  data(){
    return {
      p4prankings: []
    }

  },

  methods: {

    // promises

      async fetchFighters(){
          const res = await fetch('http://localhost:5959/p4prankings')
          const data = await res.json()
          console.log( data )
          return data
      }


  },
  async created(){
    this.p4prankings = await this.fetchFighters()
  }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}


body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 550px;
  margin: 30px auto;
  overflow: auto;
  min-height: 450px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  display: grid;
  height:100vh;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
  gap: 0.5em;
}

div{
  margin-bottom: 0.5em;
}

</style>

