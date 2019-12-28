<template>
    <!-- <v-container fluid class="">
        <v-layout wrap align-center justify-center row fill-height>
            <v-flex xs12 > -->
                 <v-carousel 
                 hide-delimiters
                 cycle
                :show-arrows="false"
                 >
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    >
     
     <v-row
            class="fill-height  overlay"
            align="center"
            justify="center"
          >
        <v-col class="text-center white--text textover" cols="12" style="">
        <h4 class="mb-2" style=" font-family: 'Roboto', sans-serif; font-size:150%; font-weight: 900;">...building community through smallholder farmers</h4>
        <h1 class="heading text-capitalize font-italic font-weight-black" style="font-size:200%; font-family: 'roboto', sans-serif;">lets walk you through a value-based agric-investment experience</h1>
      </v-col>
          </v-row>
    </v-carousel-item>
  </v-carousel>
        
</template>
<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1577427671/hero1_ynojek.jpg',
          },
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1577429435/hero43_ju7qob.jpg',
          },
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1577430407/hero344_prh1jh.jpg',
          },
          
        ],
         cycle: true,
      }
    },
  }
</script>
<style scoped>
.overlay {
      opacity: 0.9;
      
    background: rgba(129, 199, 132, 0.47);
  
    
}
.textover {
  
   text-shadow: 0px 3px 0px #b2a98f,
                 0px 14px 10px rgba(0,0,0,0.15),
                 0px 24px 2px rgba(0,0,0,0.1),
                 0px 34px 30px rgba(0,0,0,0.1);
  z-index:1;
}
</style>