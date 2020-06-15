<template>
   <v-container>
      <v-row dense>
        <v-col
          v-for="(item, i) in apps"
          :key="i"
          cols="4"
        >
          <app-card :type="item.type" :title="item.title" :data=item.value />
        </v-col>
      </v-row>
    </v-container>
</template>

<script>
import AppCard from "@/components/AppCard.vue";

  export default {
    data: () => ({
      apps: [
        { type: 'PostgreSQL', title: 'psql-1', value: [0, 2, 3, 7, 5, 6, 3, 5, 4, 0, 1, 8, 2, 9, 0] },
        { type: 'PostgreSQL', title: 'psql-2', value: [0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0]},
        { type: 'Redis', title: 'redis-1', value: [10, 8, 7, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0]},
        { type: 'Elasticsearch', title: 'elastic-ocelot', value: [0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0]},
        { type: 'MongoDB', title: 'lonely-seahorse', value: [0, 2, 5, 9, 5, 10, 3, 5, 0, 0, 1, 8, 2, 9, 0]},
      ],
    }),
    components: {
      AppCard: AppCard
    }
  }
</script>
