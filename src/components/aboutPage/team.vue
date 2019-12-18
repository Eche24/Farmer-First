<template>
  <v-container>
    <h1 class="subheading blue--text">Team</h1>
    <v-layout row wrap fill-height>
      <v-flex xs12 sm6 md6 lg4 v-for="person in speakers2019" :key="person.id">
        <v-card class="text-xs-center ma-3 mx-auto" max-width="344" height=370 flat >
          <v-responsive class="pt-4">
            <v-avatar size="150" class="grey lighten-2">
              <v-img 
             
              :src="require('~/assets/img/team/avatar.png')"
              :lazy-src="require('~/assets/img/team/avatar.png')"
              >
                <v-layout slot="placeholder" fill-height align-center justify-center ma-0>
                  <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-layout>
              </v-img>
            </v-avatar>
          </v-responsive>
          <v-card-text>
            <div class="subheading google-font">{{person.name}}</div>
             <div class="blue-grey--text text-xs-center font-weight-light google-font" >{{person.role}}</div>
            <div class="grey--text font-weight-medium google-font">{{person.desc}}</div>
          </v-card-text>

          <v-btn class="mt-0 mx-0" icon :href="person.twitterUrl" target="_blank">
            <v-icon small center style="color:#1da1f2">fab fa-twitter</v-icon>
          </v-btn>

          <v-btn class="mt-0 mx-0" icon :href="person.linkedinUrl" target="_blank">
            <v-icon small center style="color:#0077b5">fab fa-linkedin-in</v-icon>
          </v-btn>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>

export default {
  data() {
    return {
      speakers2019: [
            {
                name: "lolo moto todysy",
                 role: "cfo",
                desc: "Eli drives Apptopia’s strategic vision and manages investor relations. Before Apptopia Eli was involved in several startups, including: GPush,",
                twitterUrl:"",
                facebookUrl:"",
                linkedinUrl:"",
                img: "~/assets/img/team/avatar.png"
            },
               {
                name: "lorme omkemn llo",
                 role: "cfo",
                desc: "Eli drives Apptopia’s strategic vision and manages investor relations. Before Apptopia Eli",
                twitterUrl:"",
                facebookUrl:"",
                linkedinUrl:"",
                img: "~/assets/img/team/avatar.png"
            },
               {
                name: "lorem ben ominn",
                 role: "cfo",
                desc: "Eli drives Apptopia’s strategic vision and manages investor relations. Before Apptopia Eli",
                twitterUrl:"",
                facebookUrl:"",
                linkedinUrl:"",
                img: "~/assets/img/team/avatar.png"
            },

      ],
      tile: false,
      img: true,
      
    };
  },
  
};
</script>