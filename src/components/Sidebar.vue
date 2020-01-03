<template>
    <div class="sidebar w-1/6 absolute top-5 z-10">
        <div id="moreAmenity" @click="moreAmenityList = !moreAmenityList, hideDetails()" class="button bg-primary flex flex-row justify-between items-center w-5/6 text-white uppercase tracking-widest text-xs cursor-pointer rounded-r-full px-2 py-1 relative select-none">
            <span>More Amenities </span>
            <i class="fas text-white" :class="[moreAmenityList == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
            <div class="arrow right absolute" v-if="moreAmenityList"></div>
        </div>
        <div class="detail cec absolute bg-white px-3 py-2 rounded-r-lg" v-if="isCEC">
            <span @click="hideDetails()" class="closeBtn cursor-pointer absolute bg-primary text-white rounded-full float-right text-xs flex justify-center items-center">X</span>
            <p class="pr-4 mb-2">
                Weather you choose a car less lifestyle or your car is in  for service, 
                the Vespaio community car is a great convenience.  
                Just download the mobile app, create an account, click and drive.  Fees apply.
            </p>
            <img src="../assets/imgs/detail/cec.png" class="w-full" alt="">
        </div>

        <div class="detail shp absolute bg-white px-3 py-2 rounded-r-lg" v-if="isSmartHomePkg">
            <span @click="hideDetails()" class="closeBtn cursor-pointer absolute bg-primary text-white rounded-full float-right text-xs flex justify-center items-center">X</span>
            <p class="pr-4 mb-2">
                Weather you choose a car less lifestyle or your car is in  for service, 
                the Vespaio community car is a great convenience.  
                Just download the mobile app, create an account, click and drive.  Fees apply.
            </p>
            <img src="../assets/imgs/detail/cec.png" class="w-full" alt="">
        </div>

        <div class="detail ffa absolute bg-white px-3 py-2 rounded-r-lg" v-if="isFrndFmlyApt">
            <span @click="hideDetails()" class="closeBtn cursor-pointer absolute bg-primary text-white rounded-full float-right text-xs flex justify-center items-center">X</span>
            <p class="pr-4 mb-2">
                Weather you choose a car less lifestyle or your car is in  for service, 
                the Vespaio community car is a great convenience.  
                Just download the mobile app, create an account, click and drive.  Fees apply.
            </p>
            <img src="../assets/imgs/detail/cec.png" class="w-full" alt="">
        </div>

        <div class="detail dpl absolute bg-white px-3 py-2 rounded-r-lg" v-if="isDigiPkgLock">
            <span @click="hideDetails()" class="closeBtn cursor-pointer absolute bg-primary text-white rounded-full float-right text-xs flex justify-center items-center">X</span>
            <p class="pr-4 mb-2">
                Weather you choose a car less lifestyle or your car is in  for service, 
                the Vespaio community car is a great convenience.  
                Just download the mobile app, create an account, click and drive.  Fees apply.
            </p>
            <img src="../assets/imgs/detail/cec.png" class="w-full" alt="">
        </div>

        <div class="detail sba absolute bg-white px-3 py-2 rounded-r-lg" v-if="isSmartBuildAccess">
            <span @click="hideDetails()" class="closeBtn cursor-pointer absolute bg-primary text-white rounded-full float-right text-xs flex justify-center items-center">X</span>
            <p class="pr-4 mb-2">
                Weather you choose a car less lifestyle or your car is in  for service, 
                the Vespaio community car is a great convenience.  
                Just download the mobile app, create an account, click and drive.  Fees apply.
            </p>
            <img src="../assets/imgs/detail/cec.png" class="w-full" alt="">
        </div>

        <div class="detail evc absolute bg-white px-3 py-2 rounded-r-lg" v-if="isEVCharging">
            <span @click="hideDetails()" class="closeBtn cursor-pointer absolute bg-primary text-white rounded-full float-right text-xs flex justify-center items-center">X</span>
            <p class="pr-4 mb-2">
                Weather you choose a car less lifestyle or your car is in  for service, 
                the Vespaio community car is a great convenience.  
                Just download the mobile app, create an account, click and drive.  Fees apply.
            </p>
            <img src="../assets/imgs/detail/cec.png" class="w-full" alt="">
        </div>

        <div class="detail solAr absolute bg-white px-3 py-2 rounded-r-lg" v-if="isSolarArray">
            <span @click="hideDetails()" class="closeBtn cursor-pointer absolute bg-primary text-white rounded-full float-right text-xs flex justify-center items-center">X</span>
            <p class="pr-4 mb-2">
                Weather you choose a car less lifestyle or your car is in  for service, 
                the Vespaio community car is a great convenience.  
                Just download the mobile app, create an account, click and drive.  Fees apply.
            </p>
            <img src="../assets/imgs/detail/cec.png" class="w-full" alt="">
        </div>

        <div class="detail dcs absolute bg-white px-3 py-2 rounded-r-lg" v-if="isDigiConServ">
            <span @click="hideDetails()" class="closeBtn cursor-pointer absolute bg-primary text-white rounded-full float-right text-xs flex justify-center items-center">X</span>
            <p class="pr-4 mb-2">
                Weather you choose a car less lifestyle or your car is in  for service, 
                the Vespaio community car is a great convenience.  
                Just download the mobile app, create an account, click and drive.  Fees apply.
            </p>
            <img src="../assets/imgs/detail/cec.png" class="w-full" alt="">
        </div>
        
        <div class="list bg-white p-2 py-4 rounded-r-lg select-none" v-if="moreAmenityList">
            <ul class="text-xs relative select-none">
                <li class="text-xs pb-2 pt-2 cursor-pointer relative" @click="hideDetails(), isCEC = true">
                    <span>Commuity Electric Car</span> <i class="fal ml-1" :class="[isCEC == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
                </li>
                <li class="text-xs pb-2 cursor-pointer relative" @click="hideDetails(), isSmartHomePkg = true">
                    <span>Available Smart Home Packages</span> <i class="fal ml-1" :class="[isSmartHomePkg == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
                </li>
                <li class="text-xs pb-2 cursor-pointer relative" @click="hideDetails(), isFrndFmlyApt = true">
                    <span>Friends & Family Apartment</span> <i class="fal ml-1" :class="[isFrndFmlyApt == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Outdoor Movie Theater</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer relative" @click="hideDetails(), isDigiPkgLock = true">
                    <span>Digital Package Lockers</span> <i class="fal ml-1" :class="[isDigiPkgLock == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
                </li>
                <li class="text-xs pb-2 cursor-pointer relative" @click="hideDetails(), isSmartBuildAccess = true">
                    <span>Smart Building Access</span> <i class="fal ml-1" :class="[isSmartBuildAccess == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
                </li>
                <li class="text-xs pb-2 cursor-pointer relative" @click="hideDetails(), isEVCharging = true">
                    <span>EV Charging Stations</span> <i class="fal ml-1" :class="[isEVCharging == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
                </li>
                <li class="text-xs pb-2 cursor-pointer relative" @click="hideDetails(), isSolarArray = true">
                    <span>96 KW Solar Array</span> <i class="fal ml-1" :class="[isSolarArray == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Two Fire Pits</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Jacuzzi</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Pet Park</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Common Area Wi-Fi</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Gated Parking</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer relative" @click="hideDetails(), isDigiConServ = true">
                    <span>Digital Concierge Service</span> <i class="fal ml-1" :class="[isDigiConServ == true ? 'fa-minus-circle' : 'fa-plus-circle ']"></i>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Fitness Parcoursse</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Community App & Social Platform</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Fitness & Wellness Classes</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Community Social Events</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Sustainable Building Design</span>
                </li>
                <li class="text-xs pb-2 cursor-pointer">
                    <span>Community Art</span>
                </li>
                <li class="text-xs cursor-pointer">
                    <span>RO Drinking Water</span>
                </li>
            </ul>
        </div>
    </div>    
</template>

<script>
import jQuery from 'jquery'
global.jQuery = jQuery 
export default {
  name: 'Sidepanel',
  data: function() {
    return {
        moreAmenityList: true,
        isCEC: false,
        isSmartHomePkg: false,
        isFrndFmlyApt: false,
        isDigiPkgLock: false,
        isSmartBuildAccess: false,
        isEVCharging: false,
        isSolarArray: false,
        isDigiConServ: false
    }
},
  methods:{
        hideDetails(){
          this.isCEC = false;
          this.isSmartHomePkg = false;
          this.isFrndFmlyApt = false;
          this.isDigiPkgLock = false;
          this.isSmartBuildAccess = false;
          this.isEVCharging = false;
          this.isSolarArray = false;
          this.isDigiConServ = false;
      }
  },
  mounted () {
    this.$nextTick(() => {
      let btnHeight = jQuery('#moreAmenity').outerHeight();
      jQuery('#moreAmenity').css({
        top: btnHeight/2
      });
    });
  }
}
</script>


<style scoped>

.arrow {width: 0; height: 0;top:25px;right: 7px;}
.arrow.right {border-top: 0px solid transparent;border-bottom: 10px solid transparent;border-left: 12px solid var(--primary);}
.detail{width:135%;left:102%;}
.detail p {font-size: 11px;line-height: 15px;}
.cec{top:8%}
.shp {top: 13%;}
.ffa {top: 17%;}
.dpl {top:25%;}
.sba {top:30%;}
.evc{top:35%;}
.solAr {top:40%;}
.dcs {top:54%;}
span.closeBtn {
    width: 15px;
    height: 15px;font-size: 9px;
    top: 5px;
    right: 5px;
}

</style>
