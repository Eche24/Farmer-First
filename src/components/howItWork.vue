 <<template>
      <v-container fluid class="grey--text" style="background:">
          <p class=" text-center mb-0 black--text " style="font-size:190%;">Our Model</p> <br>
         <p class="text-center mb-0 blue--text" style="font-size:120%; font-family: 'Quicksand', sans-serif;">Our investment model is grouped into two parts A and B</p>
      <v-layout wrap align-center justify-center row fill-height class="my-3" >
         
       <v-flex xs12 sm6 md5 lg6 class="">  
          <v-card 
          flat 
          dense 
          height='250'
          >
          <v-card-title style="font-size:120%;">
             <p class="green--text"  > Part A (Social Farming) </p>
             </v-card-title>
      <v-card-text>
      <p style="font-family: 'Quicksand', sans-serif; font-size:120%;">
       This allows you invest in small holder farmers by subscribing to any of the farms listed here on the
        platform and upon harvest proceeds are shared to subscribers at the <B> stipulated time </b> and <b>ROI</b>.</p>
        </v-card-text>
        </v-card>
        </v-flex>

         <v-flex xs12 sm6 md6 lg6 class=""> 

            <v-card 
            flat
             dense
            height="250"
            >
          <v-card-title style="font-size:120%;">
        <p class=" green--text sub-heading"  > Part B (Contract Farming) </p>
        </v-card-title>
        <v-card-text>
       <p style="font-family: 'Quicksand', sans-serif; font-size:120%;">
       Here in, an exclusive investor uses a minimum stipulated amount to own a virtual farm for an agreeable tenure period. Within this period, whatever is produced there is shared between the investor and our
        organisation. Typically, the returns are over <b>2X higher</b>, so is the invested capital. 
    </p>
     </v-card-text>
    </v-card>
      </flex>
 
   </v-flex>
    </v-layout>

         <v-divider/>
       <v-card 
       class="mb-2 mx-auto" 
       flat
        max-width="400"
         tile
       >
           <p class="subtitle-4 text-center pt-4" style="font-size:180%;">How it work? </p>  
                 <p class="text-center mt-0 blue--text" style="font-size:; font-family: 'Quicksand', sans-serif;">Subscription Procedures:</p>
      
        <v-card-text style="font-family: 'Quicksand', sans-serif; font-size:110%" class="text-center green--text">
          <v-list rounded>
      <v-list-item-group v-model="item" color="primary">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
        </v-card-text>
      </v-card>
    </v-container>
 </template>
 <script>
  export default {
    data: () => ({
     
      items: [
        { text: 'Account Creation', icon: 'mdi-account' },
        { text: 'Choose a Farm', icon: 'mdi-feature-search' },
        { text: 'Received Updates/Historical data', icon: 'mdi-message' },
        { text: 'Get Paid', icon: 'mdi-cash-multiple' }
      ],
    }),
  }
</script>

