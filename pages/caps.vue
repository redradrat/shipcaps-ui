<template>
      <v-container fluid>
      <v-row dense>
        <v-col
          v-for="cap in caps"
          :key="cap.title"
          cols=4
        >

          <cap-card :name=cap.title :description=cap.description :icon=cap.icon :type=cap.type />

        </v-col>
      </v-row>
    </v-container>
</template>

<script lang="ts">
  import CapCard from "@/components/CapCard.vue";
  import Vue from 'vue'
  export default Vue.extend({
    data: () => ({
      caps: [
        { type: 'Cap', title: 'PostgreSQL', description: "A PostgreSQL DB instance", icon: 'https://cdn.vuetifyjs.com/images/cards/house.jpg' },
        { type: 'Cap', title: 'MySQL', description: "A MySQL DB instance", icon: 'https://cdn.vuetifyjs.com/images/cards/road.jpg'},
        { type: 'Cap', title: 'Redis', description: "A Redis Cache instance", icon: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg'},
        { type: 'ClusterCap', title: 'Elasticsearch', description: "An Elasticsearch instance", icon: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg'},
        { type: 'Cap', title: 'MongoDB', description: "A MongoDB instance", icon: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg'},
      ],
    }),
    components: {
      CapCard: CapCard
    }
  })
</script>
