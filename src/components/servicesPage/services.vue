<template>
    <v-container class="pa-0 grey--text">
        <v-layout wrap align-center justify-center row fill-height class="my-3" >
    <v-flex xs12 md12 lg12 class="pa-2">
         <!-- <p class="text-center black--text" style="font-size:150%">Our Farms</p> -->
       <v-card flat>
           <v-card-title>
               Activities of 2019
                 
           </v-card-title>
         <v-carousel :show-arrows="false">
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
          

       </v-card>    
    </v-flex>
        </v-layout>
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md12 class=" pl-2">
        <Product />
        <v-divider />
            <p class="text-center black--text" style="font-size:150%">coming soon</p>
        <Product />

         </v-flex>
           </v-layout>
    </v-container>
</template>
<script>
import Product from '~/components/servicesPage/product.vue'
import Activity from '~/components/servicesPage/activity.vue'

export default {
      components :{
        Product,
        Activity
    },
    data () {
      return {
        items: [
          {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1577427671/hero1_ynojek.jpg',
          },
          
        ],
      }
    }
}
</script>