<template>
  <v-footer
    color="#343a40"
    height="auto"
    
  >
    <v-container fluid style="" >
      <v-layout wrap align-center justify-center row fill-height class="my-0 py-0">
        <v-flex xs12 md10 sm10 lg10 class="py-0 my-0">
          <p class="google-font" style="font-size:130%;  color:#868e96;" >Follow Us:
            <span v-for="(item,i) in ChapterDetails.socialLinks" :key="i">
              <v-tooltip top>
                  <v-btn flat icon :href="item.link" target="_blank" slot="activator">
                    <v-icon>{{item.icon}}</v-icon>
                  </v-btn>
                  <span>{{item.name}}</span>
              </v-tooltip>
            </span>
          </p>
          <v-divider></v-divider>
        </v-flex>
      </v-layout>

      <v-layout wrap justify-center row>
        <v-flex xs12 md12 lg10>
           <v-layout wrap align-start justify-start row class="my-2">
            <v-flex xs12 md4 sm3 lg3 class="py-2">
              <p class="google-font mb-0" style="font-size: 140%;font-weight: 300; color:#868e96;"><b>Our Location</b></p>  
              <div v-for="(item,i) in FooterData.AboutSession" :key="i" class="mt-1" color="white">
                <a :href="item.Link" class="google-font" target="_blank" style="color: white;text-decoration: none;font-size:110%">{{item.LinkName}}</a><br>
              </div>
            </v-flex>

            <v-flex xs12 md4 sm4 lg3 class="py-2">
              <p class="google-font mb-0" style="font-size: 140%;font-weight: 300;  color:#868e96;"><b>Services</b></p>  
              <div v-for="(item,i) in FooterData.ChapterResourcesSession" :key="i" class="mt-1">
                <a :href="item.Link" class="google-font" target="_blank" style="color:white;text-decoration: none;font-size:110%">{{item.LinkName}}</a><br>
              </div>
            </v-flex>

            <v-flex xs12 md3 sm4 lg3 class="py-2">
              <p class="google-font mb-0" style="font-size: 140%;font-weight: 300; color:#868e96;"><b>Our Core Value</b></p>  
              <div v-for="(item,i) in FooterData.DevConsole" :key="i" class="mt-1">
                <a :href="item.Link" target="_blank" class="google-font" style="color: white;text-decoration: none;font-size:110%">{{item.LinkName}}</a><br>
              </div>
            </v-flex>
           </v-layout>
        </v-flex>

      </v-layout>

      <v-layout wrap justify-center row class="mb-0">
        <v-flex xs12 md10 lg10>
          <v-divider></v-divider>
           <v-toolbar flat color="#212529" class="pa-0 mx-0" style="padding:0 !important; color:white; " >
              <v-toolbar-title class="google-font pl-0 ml-0 mr-3 " style="font-size:200%; font-family: 'Baskervville', serif;"></v-toolbar-title>
               {{ new Date().getFullYear() }} - Farmer First
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
            <v-btn
            text
            :to="$url('/privacy')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
            color="white"
          >
            Privacy 
          </v-btn>
            </v-toolbar>
        </v-flex>
      </v-layout>

    </v-container>
  </v-footer>
</template>
<script>
  import ChapterDetails from '@/assets/data/chapterDetails.json'
  import FooterData from '@/assets/data/footer.json'
  export default {
    data() {
      return {
        ChapterDetails:ChapterDetails,
        FooterData:FooterData
      }
    },
  }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Baskervville&display=swap');
</style>