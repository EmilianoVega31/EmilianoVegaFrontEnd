<template>
    <div class="rankingbox">


        

        <div v-for="fighter in p4prankings" :key="fighter.number" >
            <FighterRanks :fighter="fighter"/>
        </div>

    </div>
    


</template>

<script>

    import FighterRanks from './FighterRanks.vue';


    export default{
        name: 'RankingBox',
        components: {
            FighterRanks
},
        props:{
            
            p4prankings: Array
        }
    }

</script>

<style scoped>

.rankingbox{
    display: grid;
    height:150vh;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
    gap: 0.5em;
    background-color: black;
    padding: 1em;
    color: red;
    
}

</style> 