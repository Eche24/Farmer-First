<template>
    <v-container>
        <v-layout wrap align-center justify-center row fill-height>
            <v-flex xs12 >
                 <v-carousel 
                 hide-delimiters
                 cycle
                 >
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
            </v-flex>
        </v-layout>
    </v-container>
</template>
<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576648382/1_q5aayb.jpg',
          },
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576648383/3_htg9es.jpg',
          },
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576648382/2_f4yjlz.jpg',
          },
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576648382/4_d5xw98.jpg',
          },
        ],
         cycle: true,
      }
    },
  }
</script>