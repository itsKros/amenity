<template>
    <header class="bg-gray-900 text-white flex flex-col md:flex-row justify-between px-4 py-2">
        <div class="brand uppercase w-full md:w-2/12 flex m-auto text-primary text-xl tracking-widest">
            Explore Amenties
        </div>
        <div class="amenties w-full md:w-80 flex justify-between item-center uppercase text-white overflow-x-scroll md:overflow-none">
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
        
    </header>
</template>

<script>
export default {
  name: 'Header',
  
}
</script>


<style scoped>

.amenties {width:80%}
.amenties a{font-size:12px;}
.amenties a.selected {color:var(--primary);}
.amenties .circle{height:10px;width:10px;}
.amenties a.selected .circle {background-color:var(--primary);}

</style>
