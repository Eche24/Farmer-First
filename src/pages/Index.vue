<template>
  <Layout>
 <v-container style="background-color:white" class="my-1 mt-2">
      <v-layout wrap align-center justify-center row fill-height class="mt-5">
        <v-flex xs12 md12 >
          <HomeStartScreen />
        </v-flex>
      </v-layout>
    </v-container>
  <v-container fluid style="background-color:#f6f6f7" >
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10 class="">
            <p class="" style="font-size:190%; text-align:center;"> Farmer first</p>
               <p class="google-font" style="font-size:110%; text-align:center; color: green;">
                  buiding communities through smallfolder farmer. 
               </p>
          <About />
        </v-flex>
      </v-layout>
 </v-container>
  <v-container fluid >
    
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10>
          <HowIt />
        </v-flex>
      </v-layout>
    </v-container>
      <v-container fluid >
    <v-divider />
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10>
       <Gallery />
        </v-flex>
      </v-layout>
      </v-container>
         <v-container fluid >
    
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10>
       <ContactForm />
        </v-flex>
      </v-layout>
      </v-container>
  </Layout>
</template>

<script>
 import HomeStartScreen from '~/components/hero.vue'
 import About from '~/components/about.vue'
 import HowIt from '~/components/howItWork.vue'
 import Gallery from '~/components/gallery.vue'
 import ContactForm from '~/components/form.vue'

  export default {
      components: {
      HomeStartScreen,
      About,
      HowIt,
      Gallery,
      ContactForm
    },
    metaInfo () {
      return {
        title: 'Home',
        meta: [
          { name: 'description', content: 'Landing page' },
        ],
      }
    },
  }
</script>
