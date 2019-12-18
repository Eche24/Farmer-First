<template>
  <Layout>
    
    <Contact />
  </Layout>
</template>

<script>
import Contact from '~/components/contactPage/contact.vue'
  export default {
    components :{
         Contact
    },
    metaInfo () {
      return {
        title: 'Contact Us',
        meta: [
          { name: 'description', content: 'Contact page' },
        ],
      }
    },

  }
</script>
