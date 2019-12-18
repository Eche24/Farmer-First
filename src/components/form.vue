<template>
      <v-container class="pa-0 my-0">
        <v-layout wrap align-center justify-center row fill-height class="mt-2" style="background-color:#FAFAFA">
            <!-- <v-flex xs12 sm4 md2 lg2 class="pa-4">
               
            </v-flex> -->
           <v-flex xs12 sm8 md10 lg10 class="pa-2 py-4 px-3" >
               <p class="google-font mb-0" style="font-size:150%">Send Us a Message</p>
               <p class="google-font mt-1" style="font-size:120%">
              Voluptates ipsum quia explicabo eligendi quae numquam nesciunt eaque nihil saepe vero.
               </p>
               <v-card width="600" flat class="mx-auto">
                   <v-card-text>
                 <v-form class="px-3">
                     <v-text-field label="Username" v-model="name" prepend-icon="mdi-account-circle">
                           
                     </v-text-field>
                        <v-text-field label="email" v-model="email" prepend-icon="folder" >
                           
                     </v-text-field>
                     <v-textarea label="Message" v-model="message"  prepend-icon="edit">

                     </v-textarea>
                    <v-btn text class="success mx-0 mt-3" @click="submit">
                         <v-icon class="pl-2" >send</v-icon>
                            Send us a message
                    </v-btn>
                 </v-form>
                   </v-card-text>
                   

                   
               </v-card>
            </v-flex> 
        </v-layout>

    </v-container>
</template>

<script>
export default {
    data () {
        return {
            title:"",
             email:"",
              message:"",
        }
    },
    methods: {
        submit() {
            console.log(this.title, this.email, this.message)
        }
    }
}
</script>