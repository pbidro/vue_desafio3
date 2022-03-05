<!--COMPONENT PRESENTATION-->
<template>
    <li class="element" >
        <div class="status" v-bind:class="{dead: is_dead,aliv: is_alive,unk: is_unknow}"></div>
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
        is_dead: Boolean,
        is_alive: Boolean,
        is_unknow: Boolean

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
    overflow:hidden; 
    white-space:nowrap; 

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



    .status{
        width: 20px;
        height: 20px;
        border-radius: 50%;
        border:1px black solid;
        position:absolute;
        margin-left: 147px;
        z-index: 2;
        }

            .status.dead {
    background-color: rgba(250, 202, 202, 0.965);
    }
    .status.aliv {
    background-color: rgba(201, 238, 206, 0.965);
    }
        .status.unk {
    background-color: rgba(232, 190, 243, 0.965);
    }
</style>