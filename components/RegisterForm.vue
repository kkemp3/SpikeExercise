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
      username: '',
      password: ''
    }
  },
  methods: {
    head () {
      return {
        title: 'Spike: Register'
      }
    },
    submit () {
      this.$axios.post('http://localhost:5000/register', { username: this.username, password: this.password })
        .then((Response) => { console.log(Response) })
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
