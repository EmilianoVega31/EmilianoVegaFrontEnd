<template>
    <div>
        <h1> {{pageTitle}} </h1>
        <h4> {{rankDate}} </h4>
    </div>
</template>
    
    <script>
    
    export default{
        name: 'HeaderTop',
        props:{
            pageTitle: String,
            rankDate:String
        }
    }
    
    </script>
    
    <style scoped>
    
    div{
        text-align: center;
    }
    
    </style>