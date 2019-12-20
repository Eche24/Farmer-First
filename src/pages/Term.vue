<template>
  <Layout>
  <div>
  <v-form v-model="valid" ref="form" class="px-3">
    <v-text-field label="First Name" v-model="firstname" :rules="inputRules"></v-text-field>
    <v-text-field label="Last Name" v-model="lastname" :rules="inputRules"></v-text-field>
    <v-text-field label="Email" v-model="email"></v-text-field>
    <v-btn :loading="loading" flat class="success mx-0 mt-3" @click="submit">Create Person</v-btn>
  </v-form>
  </div>
   <modal title="Add new event" effect="fade/zoom" :value="showModal" ok-text="Save" cancel-       
    text="Cancel" @ok="saveAction" @cancel="cancelAction">
        <form role="form" method="post">
            <div class="form-group">
                <label>Event name:</label>
                <input class="form-control" name="nameEvent" v-model="nameEvent">
            </div>
      </form>
    </modal>
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
