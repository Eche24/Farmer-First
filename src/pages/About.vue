<template>
  <Layout>
     <AboutPage />
    <About />
  </Layout>
</template>

<script>
import About from '~/components/aboutPage/about.vue'
 import AboutPage from '~/components/about.vue'
  export default {
     components :{
         AboutPage,
         About
    },
    
    metaInfo () {
      return {
        title: 'About us',
        meta: [
          { name: 'description', content: 'About page' },
        ],
      }
    },

  }
</script>
