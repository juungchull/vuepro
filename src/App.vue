<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
    <v-app-bar-nav-icon @click="drawer= !drawer"/>
      <site-title></site-title>
    <v-spacer/>
    <v-btn icon to="/about">
      <v-icon>mdi-magnify</v-icon>
    </v-btn>
    <v-btn icon to="/">
      <v-icon>mdi-magnify</v-icon>
    </v-btn>
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer">
      wefwef
    </v-navigation-drawer>
    <v-content>
      <router-view/>
    </v-content>
      <v-footer app color="primary" dark absolute>
    <v-spacer></v-spacer>
    <div>&copy; {{ new Date().getFullYear() }}</div>
  </v-footer>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue'
import SiteTitle from '@/views/site/title.vue'

export default Vue.extend({
  components: { SiteTitle },
  name: 'App',

  data: () => ({
    drawer: false
  })
})
</script>
