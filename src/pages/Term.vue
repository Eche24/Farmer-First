<template>
  <Layout>
 
  </Layout>
</template>

<script>
  export default {
    metaInfo () {
      return {
        title: 'Terms and Condition',
        meta: [
          { name: 'description', content: 'Terms and Condition page' },
        ],
      }
    },
     data() {
    return {
      valid: true,
      firstname: '',
      lastname: '',
      email: '',
      loading: false,
      dialog: false,
      inputRules: [
        v => (v && v.length >= 2) || 'Minimum length is 2 characters'
      ]
    }
  },
  methods: {
    submit() {
      if (this.$refs.form.validate()) {
        this.loading = true;

        const person = {
          firstname: this.firstname,
          lastname: this.lastname,
          email: this.email
        };

        /* sendToMyDB(person) */
        Promise.resolve().then(() => {
          this.loading = false;
          this.dialog = false;
          this.$refs.form.reset();
        })
      }
    }
  }

  }
</script>
