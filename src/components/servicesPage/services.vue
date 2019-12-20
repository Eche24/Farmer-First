<template>
    <v-container class="pa-0 grey--text">
        <v-layout wrap align-center justify-center row fill-height class="my-3" >
    <v-flex xs12 md6 lg6 class="pa-2">
         <p class="text-center black--text" style="font-size:150%">Our Farms</p>
       <!-- <v-card flat>
           <v-card-title>
               
                 
           </v-card-title>
           <v-card-text>
               <p class="google-font" style="font-size:110%">
                   Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus exercitationem quasi aut ea quo architecto maxime molestias, 
                   corporis qui, tempora, ratione neque recusandae veritatis nulla? Nisi minus velit eum recusandae.
               </p>
                 <p class="google-font" style="font-size:110%">
                   Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus exercitationem quasi aut ea quo architecto maxime molestias, 
                   corporis qui, tempora, ratione neque recusandae veritatis nulla? Nisi minus velit eum recusandae.
               </p>

           </v-card-text>

       </v-card>     -->
    </v-flex>
        </v-layout>
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md12 class=" pl-2">
        <Product />
    </v-flex>
           </v-layout>
    </v-container>
</template>
<script>
import Product from '~/components/servicesPage/product.vue'

export default {
      components :{
        Product
    },
}
</script>