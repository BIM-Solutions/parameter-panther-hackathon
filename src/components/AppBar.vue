<template>
  <v-app-bar app color="" dark>
    <v-img
      class="ml-2 mr-5"
      :src="require('./../assets/logo.svg')"
      max-height="80"
      max-width="80"
      contain
    ></v-img>
    <v-toolbar-title>Parameter Network</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn outlined class="mr-2" @click="$store.dispatch('logout')"> Log out </v-btn>
    <v-btn icon>
      <v-icon>mdi-heart</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>mdi-magnify</v-icon>
    </v-btn>
    <v-menu left bottom>
      <template v-slot:activator="{ on, attrs }">
        <v-btn icon v-bind="attrs" v-on="on">
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item @click="() => {}">
          <v-list-item-title>About</v-list-item-title>
        </v-list-item>
        <v-list-item @click="() => {}">
          <v-list-item-title>Workflow</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>
        
<script>
export default {
  name: "AppBar",
};
</script>

