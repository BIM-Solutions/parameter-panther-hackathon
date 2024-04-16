<template>
  <v-app-bar app color="blue" dark>
    <v-img
      class="ml-2 mr-5"
      :src="require('./../assets/logo.png')"
      max-height="40"
      max-width="40"
      contain
    ></v-img>
    <v-toolbar-title>Parameter Panther</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn outlined class="mr-2" @click="$store.dispatch('logout')"> Log out </v-btn>
  </v-app-bar>
</template>
<script>
export default {
  name: "AppBar",
};
</script>

