<template>
  <v-app dark>
    <navigation :mini=miniVariant :drawer.sync=drawer />
    <app-bar @miniVariant="miniVariant = !miniVariant" @navCollapse="drawer = !drawer" />
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer
      app
    >
      <span><a class="text-decoration-none accent--text" target="_blank" href="https://github.com/redradrat">redradrat</a> &copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script lang="ts">
import Navigation from '@/components/Navigation.vue'
import AppBar from '@/components/AppBar.vue'
import Vue from 'vue'

export default Vue.extend({
   data: () => ({
      drawer: true,
      miniVariant: false,
    }),
    components: {
      Navigation,
      AppBar
    }
})
</script>
