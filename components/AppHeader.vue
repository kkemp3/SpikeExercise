
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

          <v-btn to="/login" nuxt>
            Login
          </v-btn>

          <v-btn to="/register" nuxt>
            register
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
