<template>
  <v-container>
    <v-col sm="50">
      <v-form ref="form" lazy-validation>
        <v-text-field
          v-model="username"
          label="UserName"
          required
        />
        <v-text-field
          v-model="password"
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
      id: '',
      username: '',
      password: ''
    }
  },
  methods: {
    head () {
      return {
        title: 'Spike: Login'
      }
    },
    submit () {
      this.$axios.post('http://localhost:5000/dologin', { username: this.username, password: this.password })
        .then((Response) => {
          console.log(Response)
          this.$router.push('/homepage')
        },
        (err) => {
          console.log('Login post failed')
          this.errors.push(err)
        })
    },
    usernameToId () {
      this.id = parseInt(this.username)
    }
    // async asyncData ({ params }) {
    //   const { data } = await this.$axios.post('http://localhost:5000/login', { username: this.username, password: this.password })
    //   return { username: data.username }
    // }
  }
}

</script>

<style>
#styled-input {
    width: 100px;
}
</style>
