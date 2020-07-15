<template>
  <v-row>
    <v-col cols="12" sm="6" offset-sm="" md='12'>
      <v-card flat>
        <v-container fluid>
          <v-row>
           <NewProduct />
           <Product />
          </v-row>
        </v-container>
      </v-card>
    </v-col>
  </v-row>
</template>
<script>
import Product from '~/components/servicesPage/product.vue'
import NewProduct from '~/components/servicesPage/newProduct.vue'
export default {
  components :{
         Product,
         NewProduct  
    },
}
</script>

