<template>
    <header class="bg-gray-900 text-white flex flex-col md:flex-row justify-between px-4 py-2 relative">
        
        <div class="brand uppercase flex text-primary justify-center md:justify-start text-3xl md:text-xl tracking-widest">
            Explore Amenties
        </div>

        <div class="amenties desktop w-10/12 hidden md:flex justify-between item-center uppercase text-white overflow-x-scroll md:overflow-x-hidden">
            <a href="#" v-for="(view, index) in this.$parent.views" :key="`view-${index}`" :class="[activeViewId==view.id ? 'selected' : '']" @click="viewClicked(view)" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white">
                <span class="circle rounded-full bg-white mr-1"></span> 
                <span>{{view.name}}</span>
            </a>
        </div>

        <carousel class="block mobile" :navigationEnabled=true :paginationEnabled=false>
            <slide v-for="(view, index) in this.$parent.views" :key="`view-${index}`">
                <a href="#" :class="[activeViewId==view.id ? 'selected' : '']" @click="viewClicked(view)" class="flex justify-center items-center flex-row text-white " >
                    <span class="circle rounded-full bg-white mr-1"></span> 
                    <span>{{view.name}}</span>
                </a>
            </slide>
        </carousel>

    </header>

    
</template>

<script>
import { Carousel, Slide } from 'vue-carousel';
export default {
  name: 'Header',
  components: {
    Carousel,
    Slide
  },
  props:['activeViewId'],
  data () {
      return {
         
      }
  },
  methods: {
    viewClicked(view){
          this.$emit('viewClicked', view);
    },
      
  },
}
</script>


<style scoped>

.amenties {width:83%}
.amenties a{font-size:12px;}
a.selected {color:var(--primary);}
.circle{height:10px;width:10px;}
a.selected .circle {background-color:var(--primary);}

.mobile {display:none;}
button{
    -webkit-appearance: none !important;
border-radius: 0;
}
@media only screen and (max-width:767px){
    .desktop {display:none;}
    .mobile {display:flex;}
}


</style>
