<template>
   <v-container class="" > 
      <v-row class="fill-height" align="center" justify="center" >
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
              color="#1c2f3c"
              height="200"
              width="400"
              
            >
             
                <v-card-title class=" white--text">
                 
                  <v-icon
                    
                    left
                    color="green"
                  >
                    {{item.icon}}
                  </v-icon>
                  <span class="font-weight-light" > {{ item.name }} </span>
             
                </v-card-title>
                <v-card-text>
             
                      <p class="font-weight-bolder   white--text">
                        {{ item.text }}
                      </p>            
                </v-card-text>       
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
        
        {name:'Time and Dedication', text: 'Time and Dedication We help with the neccesary attention on the farm...', icon: 'mdi-feature-search' },
        {name:'Insurance', text: 'With our insurance cover, we have taken steps to prevent loss of invested finances and the projected returns   ',  icon: 'mdi-account' },
        { name:'Fertilizer Management', text: 'Our farm experts understand how the application of fertilizer and manure to the farm works..  ', icon: 'mdi-message' },
        {name:'Seed Management', text: 'Access to good quality of grains for planting/ processing   ', icon: 'mdi-cash-multiple' }
        
        ]
    }),
  }
</script>
 