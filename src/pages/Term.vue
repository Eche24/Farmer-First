<template>
  <Layout>
 <v-container fluid class="mt-2 mb-0">
     <p class="text-uppercase text-center mb-2 mt-2 headline" style="font-size:170%; color:#c4c01a;">terms and condition</p> 
      <v-layout wrap align-start justify-center row fill-height class="my-0">
        <v-flex xs12 md10 class="mb-0"> 
  <v-expansion-panels focusable>
    <v-expansion-panel
      v-for="(item,i) in 5"
      :key="i"
    >
      <v-expansion-panel-header>Item</v-expansion-panel-header>
      <v-expansion-panel-content>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
        </v-flex>
      </v-layout>
 </v-container>
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
