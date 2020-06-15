<template>
  <v-container>
        <v-container>
          <v-list-item two-line :class="miniVariant && 'px-0'">
            <v-list-item-avatar>
              <img src="https://randomuser.me/api/portraits/men/81.jpg">
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title>Application</v-list-item-title>
              <v-list-item-subtitle>Subtext</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

        </v-container>
  </v-container>
</template>

<script>
  export default {
  }
</script>

<style>
  .ShipcapsLogo {
    height:50px;
    width: 50px;
  }
</style>
