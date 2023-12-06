<template>
    <div>
        <h1> {{name}} </h1>
        <h4> {{domains}} </h4>
        <h4><a :href= "web_pages" >{{web_pages}}</a></h4>
        <h4> {{ country }}</h4>
        <h4> {{ alpha_two_code }}</h4>
    </div>
    </template>
    
    <script>
    
    export default{ // Exporting Default Object
        name: 'MyHeader',
        props:{ 
    
            name:String,
            domains:String,
            web_pages: String,
            country:String,
            alpha_two_code : String
        }
    }
    
    </script>
    
    <style scoped>
    
    h4{
    margin: 2px;
}

div{
    background-color: #9ea8ff;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    margin-bottom: .5em;
    

}
    
    </style>