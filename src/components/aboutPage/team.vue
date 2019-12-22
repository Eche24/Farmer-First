<template>
  <v-container>
    <p class="text-uppercase text-center mb-2 mt-2" style="font-size:170%; color:#616161;">Meet our team</p>  
    <v-layout row wrap fill-height>
      <v-flex xs12 sm6 md6 lg4 v-for="person in speakers2019" :key="person.id">
        <v-card class="text-xs-center mx-auto mb-3" max-width="344" flat>
          <v-responsive class="pt-4 ml-5 ">
            <v-avatar size="160" class="pa-2">
              <v-img 
              :src="person.img"
              :lazy-src="person.img"
              
              >
                <v-layout slot="placeholder" fill-height align-center justify-center ma-0>
                  <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                </v-layout>
              </v-img>
            </v-avatar>
          </v-responsive>
          <v-card-text>
            <div class="subheading black--text ">{{person.name}}</div>
             <div class="blue-grey--text text-xs-center font-weight-light google-font" >{{person.role}}</div>
            <!-- <div class="grey--text font-weight-medium google-font">{{person.desc}}</div> -->
            <v-btn class="mt-0 mx-0" icon :href="person.linkedinUrl" target="_blank">
            <v-icon small center style="color:#0077b5">fa fa-linkedin</v-icon>
          </v-btn>
          </v-card-text>

          <!-- <v-btn class="mt-0 mx-0" icon :href="person.twitterUrl" target="_blank">
            <v-icon small center style="color:#1da1f2">fab fa-twitter</v-icon>
          </v-btn> -->

          
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
                name: "Iortyom Terver Derek",
                 role: "Co-Founder/Chief Financial Officer ",
                desc: "",
                twitterUrl:"",
                facebookUrl:"",
                linkedinUrl:"https://www.linkedin.com/in/iortyomterverderek/",
                img: "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576980952/Iortyom_Terver_Derek_qden6m.jpg"
            },
               {
                name: "Tuleun Aondohemba Kelvin",
                 role: "Co-Founder/Farm Lead",
                desc: "",
                twitterUrl:"",
                facebookUrl:"",
                linkedinUrl:"https://www.linkedin.com/in/tuleun-aondohemba-kelvin-195b4b96/",
                img: "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576980953/kelvin_onyat0.jpg"
            },
               {
                name: "Orjime Oliver Tsokar",
                 role: "Co-Founder/Head of Data Intelligence",
                desc: "",
                twitterUrl:"",
                facebookUrl:"",
                linkedinUrl:"https://www.linkedin.com/in/orjime-oliver-tsokar-2374a9136/",
                img: "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576980953/og_huw4ke.jpg"
            },
             {
                name: "Dexter Aondofaseer Iorkohol",
                 role: "Co-Founder/Head of Operations ",
                desc: "",
                twitterUrl:"",
                facebookUrl:"",
                linkedinUrl:"https://www.linkedin.com/in/dexter-faseer-52b784189/",
                img: "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576980953/dt_sshdh0.jpg"
            }

      ],
      tile: false,
      img: true,
      
    };
  },
  
};
</script>