<template>
    

    <div>

                        <h2>{{university.name}}</h2>
                        <h4> {{university.domains}}</h4>
                        <h4> <a :href="university.web_pages" >{{university.web_pages}}</a> </h4>
                        <h4> {{university.country}}</h4>
                        <h4> {{university.alpha_two_code }}</h4>
    </div>
</template>

<script>

export default{
    name: 'SingleUniversity',
    props:{
        university: Array
    }
}
</script>

<style scoped>

.green{
    background-color: green;
}

h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    

}

.red{
background-color: orangered !important;

}


</style>