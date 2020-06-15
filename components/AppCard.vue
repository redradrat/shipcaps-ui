<template>
  <v-card
    dark
    class="ma-2"
    max-width="344"
  >
      <v-col style="position: absolute">
        <div class="overline mb-1" v-text="type" />
        <v-list-item-title class="body-1 mb-1" v-text="title" />
      </v-col>
    <v-sparkline
      class="pt-8"
      :value="data"
      :gradient="gradient"
      :smooth="12"
      :padding="2"
      :line-width="2"
      :stroke-linecap="round"
      :gradient-direction="left"
      :fill="true"
      :type="trend"
    >
    </v-sparkline>
  </v-card>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data: () => ({
      gradient: ['red', 'orange', 'yellow'],
  }),
  props: [
    "type",
    "title",
    "data"
  ]
})
</script>
