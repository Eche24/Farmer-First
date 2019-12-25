<template>
  <Layout>
 <v-container fluid  class="">
      <v-layout wrap align-center justify-center row fill-height class="mt-">
        <v-flex xs12 md12 >
          <HomeStartScreen />
        </v-flex>
      </v-layout>
    </v-container>
  <v-container fluid style="background-color:#f6f6f7" > 
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10 class="">
            <p class="text-uppercase" style="font-size:190%; text-align:center; font-family: 'Roboto', sans-serif; font-size:40px;"> Farmer first</p>
               <p class="text-capitalize" style="font-size:140%; text-align:center; color: green; font-family: 'Quicksand', sans-serif;">
                  building communities through smallholder farmers.... 
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
    <v-divider> </v-divider>
     <v-container fluid style="background-color: #fafdfa">
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10>
          <Progress />
        </v-flex>
      </v-layout>
    </v-container>
    <v-divider />
      <v-container fluid >
    
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
 import Progress from '~/components/progress.vue'
 import Gallery from '~/components/gallery.vue'
 import ContactForm from '~/components/form.vue'

  export default {
      components: {
      HomeStartScreen,
      About,
      HowIt,
      Progress,
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
