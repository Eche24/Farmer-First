<template>
  <v-container>
    <!-- style="background:#289020;" -->
    <v-layout row wrap align-center justify-center fill-height class>
      <v-flex xs12 sm6 md6 lg4 v-for="person in products" :key="person.id">
        <v-hover v-slot:default="{ hover }">
          <v-card
            class="text-xs-center ma-3 mx-auto"
            max-width="344"
            height="420"
            :elevation="hover ? 12 : 2"
          >
            <v-img :src="person.img" :lazy-src="person.img">
              <v-layout slot="placeholder" fill-height align-center justify-center>
                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
              </v-layout>
            </v-img>

            <v-expand-transition>
              <div
                v-if="hover"
                class="d-flex transition-fast-in-fast-out green darken-2 v-card--reveal display-3 white--text"
                style="height: 100%; text-shadow: 2px 2px 2px #000;"
              >
                <p>Now Selling</p>
              </div>
            </v-expand-transition>
            <v-card-text>
              <div
                class="subheading teal--text text-capitalize title"
                style="font-family: 'Roboto', sans-serif;"
              >{{person.name}}</div>
              <div class="blue-grey--text subtitle-1">{{person.role}}</div>

              <b>Duration</b>
              <v-chip outlined class="ma-1">{{person.duration}}</v-chip>
              <b>Return</b>
              <v-chip outlined class="ma-1">{{person.return}} </v-chip>
              <br />
              <b>Minimum Price Per Lot</b>
              <v-chip outlined class="ma-1" color="success">₦{{person.price}}</v-chip>
            </v-card-text>
            <v-card-actions>
              <v-btn color="green lighten-2" text @click="reserve">Now Selling</v-btn>
            </v-card-actions>
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
          name: "Cattles",
          role: "Makurdi",
          desc:
            "Eli drivesi was involved in several startups, including: GPush,",
          duration: "12 months",
          return: "50%",
          price: "50000",
          img:
            "https://firebasestorage.googleapis.com/v0/b/study-9f8db.appspot.com/o/cattle-ranches.jpg?alt=media&token=dbe173c0-e274-45f8-a746-140c010ea0cb"
        },
        {
          name: "Commodity Trading",
          role: "Makurdi",
          desc:
            "Eli drives Apptopia’s strategic vision and manages investor relatio",
          duration: "4 Months",
          return: " 15% ",
          price: "50000",
          img:
            "https://firebasestorage.googleapis.com/v0/b/study-9f8db.appspot.com/o/commodity-trading-famerfirst.jpg?alt=media&token=fb47116f-e9a5-461b-a020-31547225c6e3"
        },
        {
          name: "Commodity Trading",
          role: "Makurdi",
          desc:
            "Eli drives Apptopia’s strategic vision and manages investor relations.",
          duration: " 6 Months",
          return: "25%",
          price: "50000",
          img:
            "https://firebasestorage.googleapis.com/v0/b/study-9f8db.appspot.com/o/commodity-trading-famerfirst.jpg?alt=media&token=fb47116f-e9a5-461b-a020-31547225c6e3"
        }
      ]
    };
  }
};
</script>
<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
  cursor: pointer;
}
</style>