<template>
  <v-card
    class="ma-2"
    max-width="344"
    min-width="200"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <div class="overline mb-4" v-text="type" />
        <v-list-item-title class="headline mb-1" v-text="name" />
        <v-list-item-subtitle v-text="description" />
      </v-list-item-content>

      <v-list-item-avatar
        tile
        size="80"
        color="grey"
      >
        <v-img
          :src=icon
          :alt=name
        />
      </v-list-item-avatar>
    </v-list-item>

    <v-card-actions>
      <v-btn color="green" text>Deploy</v-btn>
      <v-btn text>Details</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: [
    "name",
    "description",
    "icon",
    "type"
  ]
})
</script>
