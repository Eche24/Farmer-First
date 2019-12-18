<template>
  <Layout>
    <About />
  </Layout>
</template>

<script>
import About from '~/components/aboutPage/about.vue'
  export default {
     components :{
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
