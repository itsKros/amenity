<template>
  <div id="app" class="relative">
    <Header id="header"></Header>
    <Sidebar id="sidebar"></Sidebar>
    <VuePannellum id="panorama" src="https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg" hfov="400" class="relative"></VuePannellum>
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
  data: function() {
    return {
        views: [
          { id: 1, name:'Resident Lounge', pano: true, active: true, link:'https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg' },
          { id: 2, name:'Game Lounge', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg' },
          { id: 3, name:'Co-Working Space', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg' },
          { id: 4, name:'Fitness Center', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg' },
          { id: 5, name:'Pool & Cabanas', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg' },
          { id: 6, name:'Terrace Lounge', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg' },
          { id: 7, name:'View Terrace', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg' },
          { id: 8, name:'Outdoor Kitchen', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/Lounge-Panorama.jpg' },
        ],
        activeView : null,

    }
  },

  methods: {

    

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

#pano {
        width: 600px;
        height: 400px;
    }
</style>
