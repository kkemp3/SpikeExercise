
<template>
  <div>
    <v-card
      color="grey lighten-4"
      flat
      height="100px"
      tile
    >
      <v-toolbar>
        <div>
          <v-btn to="/homepage" nuxt>
            Home
          </v-btn>
          <v-btn to="/about" nuxt>
            About Me
          </v-btn>

          <v-btn right absolute to="/login" nuxt>
            Login
          </v-btn>

          <v-btn to="/register" nuxt>
            Register
          </v-btn>

          <v-btn to="/profile" nuxt>
            Profile
          </v-btn>
        </div>
      </v-toolbar>
    </v-card>
  </div>
</template>

<script>

export default {
  name: 'AppHeader',
  components: {

  },
  methods: {

  }
}
</script>

<style>

</style>
