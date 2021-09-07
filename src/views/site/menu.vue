<template>
  <v-list-item v-for="item in items" :key="item.title" :to="item.to">
    <v-list-item-content>
      {{item.title}}
    </v-list-item-content>
  </v-list-item>
</template>
<script>
export default {
  props: ['menu'],
  data () {
    return {
      items: [
        {
          title: 'home',
          to: '/'
        }
      ]
    }
  }
}
</script>
