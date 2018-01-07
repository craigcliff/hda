<template>
  <v-app id="inspire" dark>
    <v-navigation-drawer clipped fixed v-model="drawer" app>
      <v-list dense>
        <nuxt-link to="/">
          <v-list-tile >
            <v-list-tile-action>
              <v-icon>account_box</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Create New User</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </nuxt-link>
        <nuxt-link to="/reset">
          <v-list-tile >
            <v-list-tile-action>
              <v-icon>lock_open</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Unlock Account</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </nuxt-link>
        <nuxt-link to="/adgroup">
          <v-list-tile >
            <v-list-tile-action>
              <v-icon>group_add</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Add User to AD Group</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </nuxt-link>

         <nuxt-link to="/software">
          <v-list-tile >
            <v-list-tile-action>
              <v-icon>send</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Deploy Software</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </nuxt-link>
          <nuxt-link to="/desktop">
          <v-list-tile >
            <v-list-tile-action>
              <v-icon>desktop_windows</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Desktop Support</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </nuxt-link>

          <nuxt-link to="/knowledge">
          <v-list-tile >
            <v-list-tile-action>
              <v-icon>lightbulb_outline</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Knowledge Base</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </nuxt-link>
  
  
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app fixed clipped-left>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Help Desk Admin</v-toolbar-title>
    </v-toolbar>
    <nuxt/>
  
  
  
    <v-footer app fixed>
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: null
    }),
    props: {
      source: String
    }
  }
</script>