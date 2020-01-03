<template>
  <div id="app" class="relative">
    <Header id="header"></Header>
    <Sidebar id="sidebar"></Sidebar>
    <VuePannellum id="panorama" src="https://pannellum.org/images/alma.jpg" hfov=175 class="relative"></VuePannellum>
    
    
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Sidebar from './components/Sidebar.vue'
import VuePannellum from 'vue-pannellum'
import jQuery from 'jquery'
global.jQuery = jQuery 
import './assets/css/fontawesome/all.min.css'
import './assets/css/main.css'
import './assets/css/style.css'
import './assets/js/script.js'
export default {
  name: 'app',
  components: {
    Header,
    VuePannellum,
    Sidebar
  },
  mounted () {
    this.$nextTick(() => {
      let header = jQuery('#header').outerHeight();
      jQuery('#panorama').css({
        height: 'calc( 100vh - '+header+'px)'
      });
    });
  }
  
}
</script>


<style>

#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
 
}
</style>
