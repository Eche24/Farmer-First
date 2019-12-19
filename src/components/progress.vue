<template>
  <v-container class=" text-center">
      <p class="text-uppercase mb-2 mt-2 " style="font-size:130%;">Progress So Far</p>
    <v-row class="fill-height" align="center" justify="center">
      <template v-for="(item, i) in items">
        <v-col
          :key="i"
          cols="12"
          md="3"
        >
          <v-hover v-slot:default="{ hover }">
            <v-card
              :elevation="hover ? 12 : 2"
              :class="{ 'on-hover': hover }"
              color="green"
            >
              <!-- <v-img
                :src="item.img"
                height="225px"
              > -->
                  <!-- </v-img> -->
                <v-card-title class="title black--text">
                  <v-row
                    class="fill-height flex-column"
                    justify="space-between"
                  >
                    <p class="mt-4 subheading text-center" style="font-size:180%;">{{ item.title }}</p>

                    <div>
                      <p class="ma-0 font-weight-bolder text-center text-capitalize white--text"  style="font-size:95%;">
                        {{ item.text }}
                      </p>
                      <!-- <p class="caption font-weight-medium font-italic text-left">
                        {{ item.subtext }}
                      </p> -->
                    </div>
                  </v-row>
                </v-card-title>
          
            </v-card>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </v-container>
</template>
<script>
  export default {
    data: () => ({
      items: [
        {
          title: '86+ ',
          text: "Acres of land Farmed ",
          subtext: '',
          img: '',
        },
        {
          title: '19+',
          text: 'Farm Subscribers ',
          subtext: '',
          img: '',
        },
        {
          title: '14+',
          text: 'Farmers Worked with ',
          subtext: 'Chill beats to mellow you out.',
          img: '',
        },
        {
          title: '180+',
          text: 'Tonnes of grain produced ',
          subtext: 'Chill beats to mellow you out.',
          img: '',
        }
      ],
      transparent: 'rgba(255, 255, 255, 0)',
    }),
  }
</script>
<style scoped>
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
 }

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>