<template>
   <v-container class="pa-0 grey--text">
        <v-layout wrap align-center justify-center row fill-height class="my-3" >
    <v-flex xs12 md6 lg6 class="pa-2">
     <v-card flat style="background-color:#f6f6f7" >
           <v-card-title>
        <p class="text-uppercase mb-0" style="font-size:130%; font-family: 'Roboto', sans-serif;">Who we are</p>
           </v-card-title>
           <v-col cols="auto">
          <v-img
            height="200"
            width="600"
            src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
          ></v-img>
        </v-col>
        <v-card-text>
    <p style="font-family: 'Roboto', sans-serif;">Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
        Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, 
        aperiam non officia eos quod asperiores</p>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit.
      Facere suscipit velit officia quae. Fuga odit consectetur tenetur
      facere accusamus iste magnam unde sapiente eos repudiandae
      nisi consequatur omnis, praesentium dolorem!
    </p>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit.
      Facere suscipit velit officia quae. Fuga odit consectetur tenetur
      facere accusamus iste magnam unde sapiente eos repudiandae
      nisi consequatur omnis, praesentium dolorem!lorem.
        <g-link class="nav__link" to="/about/">Read more</g-link>
    </p>
        </v-card-text>
         </v-card>  
      </v-flex>
       <v-flex xs12 md6 lg6 class="pa-2">
         <v-card flat style="background-color:#f6f6f7" >
           <v-card-title>
        <p class="text-uppercase" style="font-size:130%;">What we do</p>
           </v-card-title>
           <v-col cols="auto">
          <v-img
            height="200"
            width="600"
            src="https://cdn.vuetifyjs.com/images/cards/store.jpg"
          ></v-img>
        </v-col>
        <v-card-text>
    <p style="font-family: 'Quicksand', sans-serif;">Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
        Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, 
        aperiam non officia eos quod asperiores</p>
    <p style="font-family: 'Quicksand', sans-serif;">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit.
      Facere suscipit velit officia quae. Fuga odit consectetur tenetur
      facere accusamus iste magnam unde sapiente eos repudiandae
      nisi consequatur omnis, praesentium dolorem!
    </p>
    <p style="font-family: 'Quicksand', sans-serif;">
      Lorem, ipsum dolor sit amet consectetur adipisicing elit.
      Facere suscipit velit officia quae. Fuga odit consectetur tenetur
      facere accusamus iste magnam unde sapiente eos repudiandae
      nisi consequatur omnis, praesentium dolorem!
        <g-link class="nav__link" to="/about/">Read more</g-link>
    </p >
        </v-card-text>
         </v-card>  
      </v-flex>
    </v-layout>
    </v-container>
</template>