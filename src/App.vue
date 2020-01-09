<template>
  <div id="app" class="relative" v-if="this.activeView !=null">
     
    <Header :activeViewId="this.activeView.id" id="header" @viewClicked="viewClickedHandler"></Header>
    <Sidebar id="sidebar"></Sidebar>
    <div >
      <div v-show="this.activeView.pano">
        <VuePannellum id="panorama" :src="activeView.link"  class="relative"></VuePannellum>
      </div>
      <div v-show="!this.activeView.pano">
        <div id="panorama" class="bg-img" :style="{'background': 'url(' + activeView.link + ') center center no-repeat'}"></div>
        
      </div>
    </div>
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
import { get } from 'http'
export default {
  name: 'app',
  components: {
    Header,
    VuePannellum,
    Sidebar
  },
  computed:{
    cssVars() {
      return {
        'background': this.bgColor,
        '--height': this.height + 'px'
      }
    }
  },
  data: function() {
    return {
        views: [
          { id: 1, name:'Resident Lounge', pano: true, active: true, link:'https://prototypes.ssquares.co.in/panorama/1_LoungePanorama.jpg' },
          { id: 2, name:'Game Lounge', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/2_Game_Lounge.png' },
          { id: 3, name:'Co-Working Space', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/3_Coworking.png' },
          { id: 4, name:'Fitness Center', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/4_Fitness.png' },
          { id: 5, name:'Pool & Cabanas', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/5_Pool.png' },
          { id: 6, name:'Terrace Lounge', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/6_TerraceLounge.png' },
          { id: 7, name:'View Terrace', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/7_ViewTerrace.png' },
          { id: 8, name:'Outdoor Kitchen', pano: false, active: false, link:'https://prototypes.ssquares.co.in/panorama/8_OutdoorKitchen.png' },
        ],
        activeView : { id: 1, name:'Resident Lounge', pano: true, active: true, link:'https://prototypes.ssquares.co.in/panorama/1_LoungePanorama.jpg' },
    }
  },

  methods: {
      viewClickedHandler: function (e){
        this.activeView = e;
          console.log(e);
      }  
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
:root {
      --hero-image: url('{{activeView.link}}');
    }
#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.bg-img{
  height: calc(100vh - 46px) !important;background-size: cover !important;
}
#pano {
        width: 600px;
        height: 400px;
    }

    
</style>
