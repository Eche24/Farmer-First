<template>
  <v-container style="background:#289020;">
        <p class="text-uppercase mb-2 mt text-center" style="font-size:190%; color:#c4c01a;">Our Products</p>
    <v-layout row wrap fill-height class="pb-4">
      <v-flex xs12 sm6 md6 lg4 v-for="person in products" :key="person.id">
         <v-hover v-slot:default="{ hover }">
        <v-card class="text-xs-center ma-3 mx-auto" max-width="344" height=420
        :elevation="hover ? 12 : 2"
        >
          <!-- <v-responsive class="pt-4 pl-5"> -->
            <!-- <v-avatar size="250" class="grey lighten-2" tile> -->
              <v-img 
             
              :src='person.img'
              :lazy-src='person.img'
              >
                <v-layout slot="placeholder" fill-height align-center justify-center >
                  <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-layout>
              </v-img>
            <!-- </v-avatar> -->
          <!-- </v-responsive> -->
          <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out red darken-2 v-card--reveal display-3 white--text"
            style="height: 100%;"
          >
          <p> closed </p> 
          </div>
        </v-expand-transition>
          <v-card-text>
            <div class="subheading teal--text text-capitalize title" style="font-family: 'Roboto', sans-serif;">{{person.name}}</div>
             <div class="blue-grey--text subtitle-1" >{{person.role}}</div>
           
           <b>Duration</b>  <v-chip outlined class="ma-1">{{person.duration}}</v-chip>
            <b>Return </b><v-chip outlined class="ma-1">{{person.return}}</v-chip><br>
            <b>Price</b> <v-chip outlined class="ma-1"  color="success">₦{{person.price}}</v-chip>
          </v-card-text>
        </v-card>
         </v-hover>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>

export default {
  data() {
    return {
      products: [
            {
                name: "carrot",
                 role: "makurdi",
                desc: "Eli drivesi was involved in several startups, including: GPush,",
                duration:"4 months",
                return:"15%",
                price:"47000",
                img: "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576702683/bauernhofprodukte_xxiohr.jpg"
            },
               {
                name: "rice",
                 role: "cfo",
                desc: "Eli drives Apptopia’s strategic vision and manages investor relatio",
                 duration:"",
                return:"",
                price:"",
                img: "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576702681/MarketVegetablesMain-1_nxka4z.jpg"
            },
               {
                name: "lorem ben ominn",
                 role: "cfo",
                desc: "Eli drives Apptopia’s strategic vision and manages investor relations.",
                duration:"",
                return:"",
                price:"",
                img: "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576702681/images_hdooxt.jpg"
            }

      ],
     
      
    };
  },
  
};
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
</style>