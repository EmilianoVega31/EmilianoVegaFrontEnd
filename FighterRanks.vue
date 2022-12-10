<template>

    
    
        <h2> {{fighter.number}}</h2>
        <h2> {{fighter.name}}</h2>
        <h4>{{fighter.nationality}}</h4>
        <h4>{{fighter.weight}}</h4>
        <h4>{{fighter.fighter}}</h4>
    

</template>

<script>


export default{
    name: 'FighterRanks',
    props:{
        fighter: Object
    }
}


</script>

<style scoped>


h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
}



</style>