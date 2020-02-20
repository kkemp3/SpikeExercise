<template>
  <v-container>
    <v-col sm="50">
      <v-form ref="form" lazy-validation>
        <v-text-field
          v-model="loginInfo.username"
          :rules="usernameRules"
          label="UserName"
          required
        />
        <v-text-field
          v-model="loginInfo.password"
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
  data () {
    return {
      loginInfo: [
        { username: 'kevin' },
        { password: '123' }
      ]
    }
  },
  methods: {
    head () {
      return {
        title: 'Spike: Login'
      }
    },
    submit () {
      this.$axios.post('http://localhost:5000/register', this.loginInfo)
        .then((Response) => {})
        .catch((err) => {
          this.errors.push(err)
        })
    }
  }
}

</script>

<style>
#styled-input {
    width: 100px;
}
</style>
