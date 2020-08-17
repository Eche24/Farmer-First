<template>
    <v-container class="pa-0 grey--text">
        <v-layout wrap align-center justify-center row fill-height class="my-3" >
    <v-flex xs12 md12 lg12 class="pa-2">
         <!-- <p class="text-center black--text" style="font-size:150%">Our Farms</p> -->
       <v-card flat>
           <p class="text-uppercase mb-2 mt text-center" style="font-size:190%; color:#c4c01a;">
              Gallery of our  2019 activities 
                 
           </p>
         <v-carousel :show-arrows="true">
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
        <p class="text-uppercase mb-2 mt text-center" style="font-size:190%; color:#c4c01a;">Our Products</p>
        <v-flex xs12 md12 class=" pl-2">
        <NewProduct />
        <Product />
        <!-- <v-divider />
            <p class="text-center pt-2" style="font-size:150%; color:#c4c01a;">Coming Soon</p>
        <ComingSoon /> -->

         </v-flex>
           </v-layout>
    </v-container>
</template>
<script>
import Product from '~/components/servicesPage/product.vue'
import NewProduct from '~/components/servicesPage/newProduct.vue'
import Activity from '~/components/servicesPage/activity.vue'
import ComingSoon from '~/components/servicesPage/comingSoon.vue'

export default {
      components :{
        Product,
        NewProduct,
        Activity,
        ComingSoon
    },
    data () {
      return {
        items: [
         
           {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1577715890/farmerFirst-activities-2_dzk79x.jpg',
          },
           {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1577716430/farmerfirst-activity-2019_d3fxrk.jpg',
          },
           {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1577716741/farmerFirst-activities-2019-2_nbrjft.jpg',
          },
            {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1577717627/farmerfirstactivities-2019_oruqi5.jpg',
          }
          ,
            {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597609410/farmer%20first/farmer-first-activity-1_mq3kje.jpg',
          },
            {
            src: 'https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597610944/farmer%20first/soyabean-farmer-first_kzybf1.jpg',
          }
          
        ],
      }
    }
}
</script>