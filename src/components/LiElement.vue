<!--COMPONENT PRESENTATION-->
<template>
    <li class="element" v-bind:class="{ favorite: fav }">
        <img class="change" v-bind:src="img"/>
        <h3>{{name}}</h3>

    </li>
</template>

<!--COMPONENT LOGIC-->
<script>
export default {
    name: 'LiElement',
    props: {
        img: String,
        name: String,
        number: Number,
        fav: Boolean,
        fantasma: Boolean,
    },
}
</script>

<!--STYLES THAT APPLIES ONLY FOR THIS COMPONENT-->
<style scoped>
    .element {
    width: 250px;
    display: flex;
    flex-direction: column;
    justify-content: initial;
    align-items: center;
    padding: 13px;
    border-radius: 10px;
    background-color: rgb(212, 208, 208,0.965);
    margin-top: 20px;

    }
    .element:hover{

    background-color: rgba(131, 121, 121, 0.63);
    color:white;
    
    
    }   
    .element:hover > .change{

        border: 3px solid rgb(247, 247, 247);
    
    }

    
    h3 {
        font-size:1.25rem;
        text-align: center;
        font-family: Patrick Hand SC;

    }
    p {
        color: black;
    }
    img {
        width: 96px;
        border-radius: 50px;
        margin-bottom:10px;
        border: 3px solid rgb(15, 12, 12);

    }


    .element.favorite {
        background-color: black;
    }
    .element.favorite h2{
        color: white;
    }
    .element.favorite p{
        color: white;
    }
    .element.favorite img{
        width: 120px;
        border-radius: 10px;
    }
</style>