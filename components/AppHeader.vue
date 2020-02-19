
<template>
  <v-card
    color="grey lighten-4"
    flat
    height="100px"
    tile
  >
    <v-toolbar >

    <div>

      <v-btn to="/login" nuxt >
      Login
      </v-btn>

      <v-btn to="/about" nuxt >
      About Me
      </v-btn>
      <v-btn to="/homepage" nuxt>
      Home
      </v-btn>
    </div>

    </v-toolbar>
  </v-card>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>
