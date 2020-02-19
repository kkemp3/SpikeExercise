
<template>
  <v-card
    color="grey lighten-4"
    flat
    height="200px"
    tile
  >
    <v-toolbar prominent extended>

      <v-toolbar-title>Navigation</v-toolbar-title>

      <v-btn>
        <nuxt-link to="/login">Login</nuxt-link>
      </v-btn>

      <v-btn>
        <nuxt-link to="/about">About Me</nuxt-link>
      </v-btn>

    </v-toolbar>
  </v-card>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>
