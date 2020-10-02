<template>
  <v-container fluid class="mt-2 mb-0">
    <v-layout wrap align-start justify-center row fill-height class="my-0">
      <v-flex xs12 sm4 md4 lg4 class="mb-0">
        <v-card flat class="mr-5">
          <!-- <v-card-title> -->
          <p
            class="text-uppercase text-center"
            style="font-size:160%; color:#c4c01a;"
          >Contact farmer first</p>
          <!-- </v-card-title> -->
          <v-card-text>
            <p class="mb-0 mt-0" style="font-size:140%;color:#2c592a">How To Reach Us:</p>
            <p class="font-weight-bold" style="font-size:110%">Phone : +2347055387074</p>
            <!-- <p class="font-weight-bold" style="font-size:110%">Email : Spwesn@gmail.com</p> -->
            <v-divider></v-divider>
            <p class="google-font mb-0 mt-3" style="font-size:140%;color:#2c592a">Where to Find us:</p>
            <p
              class="font-weight-bold"
              style="font-size:110%"
            >Suit 6 Ashby House Wurukum,Makurdi, Benue State.</p>
            <!-- <p class="google-font mt-3" style="font-size:110%"></p> -->
          </v-card-text>
        </v-card>
      </v-flex>
      <v-flex xs10 sm7 md7 lg7 class>
        <v-card max-width="800" max-height="400" class="mx-auto mb-2">
          <v-row cols="auto">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m23!1m12!1m3!1d3953.614462867751!2d8.542477114777697!3d7.724447794432169!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!4m8!3e6!4m0!4m5!1s0x1050819327e7618f%3A0x37851a3ad6500a99!2sFarmer%20First%2C%20Old%20Otukpo%20Road%2C%20Wurukum%20970221%2C%20Makurdi!3m2!1d7.7244478!2d8.544665799999999!5e0!3m2!1sen!2sng!4v1589184791087!5m2!1sen!2sng"
              width="800"
              height="400"
              frameborder="0"
              style="border:0;"
              allowfullscreen
              aria-hidden="false"
              tabindex="0"
            ></iframe>
          </v-row>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
import SocialLink from "~/components/socialLink.vue";
export default {
  components: {
    SocialLink,
  },
  data() {
    return {};
  },
};
</script>