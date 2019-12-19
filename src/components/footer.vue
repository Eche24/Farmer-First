<template>
  <v-footer
    color="#343a40" 
  >
    <v-container fluid style="" >
        <SocialLink />
      <v-layout wrap justify-center row>
        <v-flex xs12 md12 lg10>
           <v-layout wrap align-start justify-start row class="my-2">
            <v-flex xs12 md4 sm3 lg3 class="py-2">
              <v-card  color="#343a40" flat>
                <v-card-title>
              <p class="google-font mb-0" style="font-size: 120%;font-weight: 300; color:#868e96; font-family: 'Quicksand', sans-serif;"><b>Our Location</b></p>  
                </v-card-title>
              <v-card-text>
                <ul v-for="(item,i) in FooterData.AboutSession" :key="i" class="mt-1" color="white">
                  <li class="google-font link" target="_blank" style="color: white;text-decoration: none;font-size:110%">{{item.LinkName}}</li>
                </ul>
             
              </v-card-text>
              </v-card>
            </v-flex>

            <v-flex xs12 md4 sm4 lg3 class="py-2">
              <v-card color="#343a40" flat>
               <v-card-title>
              <p class="google-font mb-0" style="font-size: 140%;font-weight: 300;  color:#868e96; font-family: 'Quicksand', sans-serif;"><b>Services</b></p> 
               </v-card-title>
               <v-card-text> 
                 <ul  v-for="(item,i) in FooterData.ChapterResourcesSession" :key="i" class="mt-1">
                   <li class="link">
                     <a :href="item.Link" class="" target="_blank" style="color:white;text-decoration: none;font-size:110%" >{{item.LinkName}}</a>
                   </li>
                 </ul>
             
               </v-card-text>
              </v-card>
            </v-flex>

            <v-flex xs12 md3 sm4 lg3 class="py-2">
             <v-card color="#343a40" flat>
               <v-card-title>
              <p class="google-font mb-0" style="font-size: 140%;font-weight: 300; color:#868e96; font-family: 'Quicksand', sans-serif;"><b>Our Core Value</b></p> 
               </v-card-title>
              <v-card-text>
             <ul v-for="(item,i) in FooterData.DevConsole" :key="i" class="mt-1">
               <li style="font-size: 110%;font-weight: 300; color:white;"> {{item.LinkName}}</li>
             </ul>
              </v-card-text>
             </v-card>
            </v-flex>
           </v-layout>
        </v-flex>

      </v-layout>

      <v-layout wrap justify-center row class="mb-0">
        <v-flex xs12 md10 lg10>
          <v-divider></v-divider>
           <v-card color="#212529" class="pa-0 mx-0" style="padding:0 !important; color:white; " >
          
                 <v-btn
            text
            
            style="text-transform: capitalize;"
            flat
            class="ml-0"
            color="white"
          >
           copyright {{ new Date().getFullYear() }} - <span> <g-image src="@/assets/img/logo/logo4.png" width="80vh" alt='farmer first logo' class="pa-0 mx-0"/></span>
          </v-btn>
         
           
      
              
            <v-btn
            text
            :to="$url('/term')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
            color="white"
          >
            Terms and Conditions
          </v-btn>
            <!-- <v-btn
            text
            :to="$url('/privacy')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
            color="white"
          >
            Privacy 
          </v-btn> -->
            </v-card>
        </v-flex>
      </v-layout>

    </v-container>
  </v-footer>
</template>
<script>
  import SocialLink from '~/components/socialLink.vue'
  import FooterData from '@/assets/data/footer.json'
  export default {
     components :{
         SocialLink    
    },
    data() {
      return {
       
        FooterData:FooterData
      }
    },
  }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Baskervville&display=swap');
.link {
  list-style-type: none;
}
</style>