<template>
  <v-app id="parameter-panther">
    <app-bar />
    <v-main>
      <router-view />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import AppBar from "./components/AppBar.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",

  components: {
    AppBar,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>
