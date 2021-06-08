<template>
  <NavBar/>
  <router-view/>
</template>

<script>
import NavBar from './components/NavBar'

export default {
  name: 'app',
  components: {
    NavBar
  }

}
</script>

<style>
#app {
  font-family: Overpass, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}



/*Scroll */

::-webkit-scrollbar{
    width: 8px;
}
::-webkit-scrollbar-track {
    box-shadow: inset 0 0 6px rgba(0,0,0,0.3);
    border-radius: 10px;
}
::-webkit-scrollbar-thumb {
    border-radius: 12px;
    background-color:  #fca211d5;
}



</style>
