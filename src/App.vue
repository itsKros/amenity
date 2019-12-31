<template>
  <div id="app">
    <Header></Header>
    <VuePannellum src="assets/panorama/Lounge-Panorama.jpg" class=""></VuePannellum>
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import VuePannellum from 'vue-pannellum'
import './assets/css/main.css'
import './assets/css/style.css'
import './assets/js/script.js'
export default {
  name: 'app',
  components: {
    Header,
    VuePannellum
  },
  
}
</script>


<style>

#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
 
}
</style>
