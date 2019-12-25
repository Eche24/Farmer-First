<template>
    <v-container fluid class="">
        <v-layout wrap align-center justify-center row fill-height>
            <v-flex xs12 >
                 <v-carousel 
                 hide-delimiters
                 cycle
                 class="overlay"
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
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576847174/IMG_20190816_113052_x19g09.jpg',
          },
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576648383/3_htg9es.jpg',
          },
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1576847799/DSCN9914-2_rmuofu.jpg',
          },
          
        ],
         cycle: true,
      }
    },
  }
</script>
<style scoped>
.overlay {
      opacity: 0.3;
    background: linear-gradient(#ff5e7c, #c272d4);
}
</style>