<template>
  <Layout>
 <v-container fluid  class="pt-0">
      <v-layout wrap align-center justify-center row fill-height class="mt-">
        <v-flex xs12 md12 lg12 >
          <HomeStartScreen />
        </v-flex>
      </v-layout>
    </v-container>
      <p class="text-capitalize pt-3" style="font-size:170%; text-align:center; color:#c4c01a; font-family: 'roboto', sans-serif;">
               Our offerings gives you leverage as you get to capitalize on.. 
      </p>
  <v-container class="pt-0" fluid style="background: #52c646;" > 
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md12 lg12 class="">
          <WhoWeAre />
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
     
    <v-divider />
      <v-container fluid class="pt-0"  style="background:#198e10;">   
              <p class="text-uppercase mb-2 mt text-center" style="font-size:190%; color:#c4c01a;">Our Products</p>
 
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
      <v-divider />
      <v-container fluid style="background-color: #fafdfa">
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10>
          <Progress />
        </v-flex>
      </v-layout>
    </v-container>
  </Layout>
</template>

<script>
 import HomeStartScreen from '~/components/hero.vue'
 import WhoWeAre from '~/components/whoWeAre.vue'
 import HowIt from '~/components/howItWork.vue'
 import Progress from '~/components/progress.vue'
 import Gallery from '~/components/gallery.vue'
 import ContactForm from '~/components/form.vue'

  export default {
      components: {
      HomeStartScreen,
      WhoWeAre,
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
