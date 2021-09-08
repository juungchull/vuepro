<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
    <v-app-bar-nav-icon @click="drawer= !drawer"/>
      <site-title :title="title"></site-title>
    <v-spacer/>
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer">

      <site-menu></site-menu>
    </v-navigation-drawer>
    <v-content>
      <router-view/>
      </v-content>
      <site-footer :footer="footer"></site-footer>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue'
import SiteTitle from '@/views/site/title.vue'
import SiteFooter from '@/views/site/footer.vue'
import SiteMenu from '@/views/site/menu.vue'

export default Vue.extend({
  components: { SiteTitle, SiteFooter, SiteMenu },
  name: 'App',

  data: () => ({
    drawer: false,
    footer: '푸터입니다.',
    title: '나의 블로그입니다.'
  })
})
</script>
