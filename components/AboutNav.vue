<template>
  <v-card height="350px">
    <v-navigation-drawer
      absolute
      permanent
      right
    >
      <template v-slot:prepend>
        <v-list-item two-line>
          <v-list-item-avatar>
            <img src="../img/pika.jpg">
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>User</v-list-item-title>
            <v-list-item-subtitle>Logged In</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </template>

      <v-divider />

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
        >
          <v-list-item-content>
            <v-btn :to="item.rdir">
              {{ item.title }}
            </v-btn>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      items: [
        { title: 'About Me', rdir: '/about' },
        { title: 'My Classes', rdir: '/classes' },
        { title: 'Future Goals', rdir: '/goals' },
        { title: 'Fun Stuff', rdir: '/fun' },
        { title: 'Other Stuff', rdir: '/other' }
      ]
    }
  }
}
</script>
