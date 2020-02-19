<template>
  <v-form ref="form" v-model="valid" lazy-validation>
    <v-text-field
      v-model="username"
      :rules="usernameRules"
      label="UserName"
      required
    />

    <v-text-field
      v-model="password"
      :rules="passwordRules"
      label="Password"
      required
    />

    <!-- <v-select
      v-model="select"
      :items="items"
      :rules="[v => !!v || 'Item is required']"
      label="Item"
      required
    ></v-select>-->

    <!-- <v-checkbox
      v-model="checkbox"
      :rules="[v => !!v || 'You must agree to continue!']"
      label="Do you agree?"
      required
    ></v-checkbox>-->

    <v-btn color="success" class="mr-4" @click="submit">
      Submit
    </v-btn>
  </v-form>
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
</style>
