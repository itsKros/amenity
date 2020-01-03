<template>
    <header class="bg-gray-900 text-white flex flex-col md:flex-row justify-between px-4 py-2 relative">
        <div class="brand uppercase flex text-primary justify-center md:justify-start text-3xl md:text-xl tracking-widest">
            Explore Amenties
        </div>
        <div class="amenties w-10/12 hidden md:flex justify-between item-center uppercase text-white overflow-x-scroll md:overflow-x-hidden">
            <a href="#" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white selected">
                <span class="circle rounded-full bg-white mr-1"></span> 
                <span>Resident Lounge</span>
            </a>
            <a href="#" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white">
                <span class="circle rounded-full bg-white mr-1"></span>
                <span>Game Lounge</span>
            </a>
            <a href="#" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white">
                <span class="circle rounded-full bg-white mr-1"></span>
                <span>Co-Working Space</span>
            </a>

            <a href="#" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white">
                <span class="circle rounded-full bg-white mr-1"></span> 
                <span>Fitness Center</span>
            </a>
            <a href="#" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white">
                <span class="circle rounded-full bg-white mr-1"></span>
                <span>Pool & Cabanas</span>
            </a>
            <a href="#" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white">
                <span class="circle rounded-full bg-white mr-1"></span>
                <span>Terrace Lounge</span>
            </a>
            <a href="#" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white">
                <span class="circle rounded-full bg-white mr-1"></span>
                <span>View Terrace</span>
            </a>
            <a href="#" class="w-1/2 md:w-auto flex justify-center items-center flex-row text-white">
                <span class="circle rounded-full bg-white mr-1"></span> 
                <span>Outdoor Kitchen</span>
            </a>
        </div>
        <carousel class="block md:hidden" :navigationEnabled=true :paginationEnabled=false>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white selected">
                    <span class="circle rounded-full bg-white mr-1"></span> 
                    <span>Resident Lounge</span>
                </a>
            </slide>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white">
                    <span class="circle rounded-full bg-white mr-1"></span>
                    <span>Game Lounge</span>
                </a>
            </slide>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white">
                    <span class="circle rounded-full bg-white mr-1"></span>
                    <span>Co-Working Space</span>
                </a>
            </slide>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white">
                    <span class="circle rounded-full bg-white mr-1"></span> 
                    <span>Fitness Center</span>
                </a>
            </slide>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white">
                    <span class="circle rounded-full bg-white mr-1"></span> 
                    <span>Fitness Center</span>
                </a>
            </slide>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white">
                    <span class="circle rounded-full bg-white mr-1"></span>
                    <span>Pool & Cabanas</span>
                </a>
            </slide>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white">
                    <span class="circle rounded-full bg-white mr-1"></span>
                    <span>Terrace Lounge</span>
                </a>
            </slide>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white">
                    <span class="circle rounded-full bg-white mr-1"></span>
                    <span>View Terrace</span>
                </a>
            </slide>
            <slide>
                <a href="#" class="flex justify-center items-center flex-row text-white">
                    <span class="circle rounded-full bg-white mr-1"></span> 
                    <span>Outdoor Kitchen</span>
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
  }
}
</script>


<style scoped>

.amenties {width:83%}
.amenties a{font-size:12px;}
a.selected {color:var(--primary);}
.circle{height:10px;width:10px;}
a.selected .circle {background-color:var(--primary);}



</style>
