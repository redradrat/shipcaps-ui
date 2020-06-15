<template>
  <v-app-bar
    fixed
    app
  >
    <v-btn icon @click.stop="$emit('miniVariant')" class="d-none d-lg-block">
      <v-icon>mdi-chevron-left</v-icon>
    </v-btn>
    <v-app-bar-nav-icon @click.stop="$emit('navCollapse')" />
    <v-spacer />
    <workspace class="align-center"/>
  </v-app-bar>
</template>

<script>
  import Workspace from '@/components/Workspace.vue'

  export default {
    data () {
      return {
        miniVariant: false,
        right: true,
      }
    },
    components: {
      Workspace
    }

  }

</script>

