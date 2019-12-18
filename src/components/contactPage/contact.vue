<template>
    <v-container fluid class="mt-2 mb-0">
      <v-layout wrap align-start justify-center row fill-height class="my-0">
        <v-flex xs12 md4 class="mb-0"> 
          <v-card flat> 
            <v-card-title>
          <p class="" style="font-size:200%;color:#616161">Contact farmer first</p>
            </v-card-title>
            <v-card-text>
             <p class="text--blue" style="font-size:150%">How To Reach Us:</p>
             <p class="font-weight-bold" style="font-size:110%">Phone : 23407035312997</p>
             <p class="font-weight-bold" style="font-size:110%">Email : Spwesn@gmail.com</p>
            </v-card-text>
          <v-divider></v-divider>
          <v-card-text>
           <p class="google-font mt-3" style="font-size:130%">Where to Find us: </p>
            <p class="google-font mt-3" style="font-size:110%">lorem at lorem to lorem oppos slloeo </p>
            <p class="google-font mt-3" style="font-size:110%">lorem at lorem to lorem oppos slloeo </p>
          </v-card-text>
             <v-divider></v-divider>
            <v-card-text>
          <p class="google-font mb-0" style="font-size:130%">Social Media:</p>
         <p class="google-font mt-3" style="font-size:110%"></p>
            </v-card-text>
          <v-card-actions>
          <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
             </v-card-actions>
          </v-card>
        </v-flex>
        <!-- <v-flex xs10 sm6 md6 lg2 class="">
          <v-card>
        <v-row cols="auto">
          <v-img
            height="200"
            width=""
            src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
          ></v-img>
        </v-row>
          </v-card>
        </v-flex> -->
      </v-layout>
    </v-container>
</template>
<script>
export default {
    components: {
    },
    data () {
        return {
      
     icons: [
        'fab fa-facebook',
        'fab fa-twitter',
        'fab fa-google-plus',
        'fab fa-linkedin',
        'fab fa-instagram',
      ],
        }
    }
}
</script>