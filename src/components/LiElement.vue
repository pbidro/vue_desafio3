<!--COMPONENT PRESENTATION-->
<template>
    <li class="element" v-bind:class="{ favorite: fav }">
        <img v-bind:src="img"/>
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
        width: 300px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-content: center;
        align-items: center;
        padding: 13px;
        border-radius: 10px;
        border: 1px solid black;
        background-color: rgb(212, 208, 208,0.965);
        margin-top: 20px;

        float:left;

    }
    h2 {
        color: black;
    }
    p {
        color: black;
    }
    img {
        width: 96px;
        border-radius: 50px;
        border: 2px solid white;
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