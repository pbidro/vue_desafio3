<template> 

<div class="container">
  <div class="row">
    <div class="col-sm " v-for="(character,index) in rickandmortyData" :key="index"
>
              <LiElement       v-bind:img="character.img"
      v-bind:name="character.name"  />

    </div>
  </div>
</div>

</template>

<script>
import LiElement from './components/LiElement'

export default {
  name: 'App',
  data() {
    return {
      rickandmortyData: [
        {
          name:'Morty Schmidt',
          img: 'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
                  },
        {          name:'Rick Sanchez',

          img: 'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
        },
        {          name:'la hermana',

          img: 'https://rickandmortyapi.com/api/character/avatar/3.jpeg'

        }
      ]
    }
  },
  components: {
    LiElement
  }
}
</script>

<style>
body{
 background-image: url("./assets/fondo.png");
 background-size: 100%;
  background-attachment: fixed;
  }

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  
}
</style>