<template>
  <v-navigation-drawer
      v-model="drawer"
      :mini-variant="mini"
      @transitionend='drawer = !drawer'
      fixed
      app
    >
    <v-list>
      <v-list-item two-line :class="mini && 'pl-2 px-0'">
        <v-img class="mr-2" src="/shipcaps-logo.png" max-width="40px" />
        <v-list-item-content>
          <v-list-item-title>Shipcaps</v-list-item-title>
          <v-list-item-subtitle>Admin</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>
    <v-divider />
    <v-list>
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :to="item.to"
        router
        exact
      >
        <v-list-item-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title v-text="item.title" />
        </v-list-item-content>
      </v-list-item>
    </v-list>

  </v-navigation-drawer>
</template>

<script lang="ts">
  import Vue from 'vue'
  export default Vue.extend({
    data: () => ({
      miniVariant: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Overview',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Caps',
          to: '/caps'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Apps',
          to: '/apps'
        }
      ],
    }),
    props: {
      drawer: Boolean,
      mini: Boolean
    }
  })
</script>
