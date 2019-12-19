<template>
      <v-container class="pa-0 my-0">
        <v-layout wrap align-center justify-center row fill-height class="mt-2" style="background-color:#FAFAFA">
            <!-- <v-flex xs12 sm4 md2 lg2 class="pa-4">
               
            </v-flex> -->
           <v-flex xs12 sm8 md10 lg10 class="pa-2  px-3" >
               <p class="google-font mb-0" style="font-size:130%">Send Us a Message</p>
               <p class="google-font mt-1" style="font-size:110%; font-family: 'Quicksand', sans-serif;">
              Voluptates ipsum quia explicabo eligendi quae numquam nesciunt eaque nihil saepe vero.
               </p>
               <v-card width="600" flat class="mx-auto">
                   <v-card-text>
                 <v-form class="px-3" ref="form">
                     <v-text-field label="Username" v-model="name" prepend-icon="mdi-account-circle" :rules="inputRules" placeholder="enter your full name">
                           
                     </v-text-field>
                        <v-text-field label="email" v-model="email" prepend-icon="folder" :rules="inputRules" placeholder="enter your email address">
                           
                     </v-text-field>
                     
                     <v-textarea label="Message" v-model="message"  prepend-icon="edit" :rules="inputRules" placeholder="enter a message">

                     </v-textarea>
                    <v-btn text class="success mx-0 mt-3" @click="submit" >
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
import db from '@/fb'
export default {
    data () {
        return {
            name:"",
             email:"",
              message:"",
              inputRules: [
                 v => v.length >= 3 || 'minimum lenght is 3 characters' 
              ]
        }
    },
    methods: {
        submit() {
           if(this.$refs.form.validate()) {
             const info = {
                 name: this.name,
                 email: this.email,
                 message: this.message
             }
              
               db.collection('info').add(info).then(() => {
                  alert('Message has been sent')
               })
              
           }
           
        }
    }
}
</script>