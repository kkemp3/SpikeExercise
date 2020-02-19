<template>
  <v-container>
    <v-col sm=50>
      <v-form ref="form" v-model="valid" lazy-validation>
        <v-text-field
          id="styled-input"
          v-model="username"
          :rules="usernameRules"
          label="UserName"
          required
        />
        <v-text-field
          id="styled-input"
          v-model="password"
          :rules="passwordRules"
          label="Password"
          type="password"
          required
        />

        <v-btn color="grey" class="mr-4" type="submit" @click="submit">
          Submit
        </v-btn>
      </v-form>
    </v-col>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    username: '',
    password: '',
    usernameRules: [
      v => !!v || 'Username is required'
    ],
    passwordRules: [
      v => !!v || 'Password is required'
    ]
  }),

  methods: {
    head () {
      return {
        title: 'Spike: Login'
      }
    },
    submit () {
      if (this.$refs.form.submit()) {
        this.submitted = true
      }
    }
  }
}
</script>

<style>
#styled-input {
    width: 100px;
}
</style>
