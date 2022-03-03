<template> 

<div class="container">
  <div class="row">
    <div class="capsule col-xs-6 col-md-4 col-lg-3 col-xl-2 " v-for="(character,index) in rickandmortyData" :key="index"
>
              <LiElement  class="crop"     v-bind:img="character.image"
      v-bind:name="character.name"  />

    </div>
  </div>
</div>

</template>

<script>
import LiElement from './components/LiElement'
import dumpdata from './data.js'

export default {
  name: 'App',
  data() {
    return {
      rickandmortyData:  dumpdata }

    
  },
  components: {
    LiElement
  }
}
</script>

<style>
*{box-sizing: border-box;}
body{
 background-image: url("./assets/fondo.png");
background-size:cover;
background-position:center;
background-repeat:no-repeat;
background-attachment: fixed;
  }

.capsule{
    display: flex;
    justify-content: center;
}

.crop{
    overflow:hidden; 
  white-space:nowrap; 
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  
}

</style>