<template>
  <Layout>
    <Services />
  </Layout>
</template>

<script>
import Services from '~/components/servicesPage/services.vue'
  export default {
     components :{
         Services
    },
    metaInfo () {
      return {
        title: 'Services',
        meta: [
          { name: 'description', content: 'services page' },
        ],
      }
    },

  }
</script>
