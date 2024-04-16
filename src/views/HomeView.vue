<template>
  <div>

    <v-container mx-0>
      <v-row no-gutters>
        <v-col md="8">
          <data-table @setRenderer="setRenderer" @applyFilter="applyFilter" />
        </v-col>
        <v-col md="4">
          <renderer :objectUrls="objectUrls" :filter="filter" />
        </v-col>
      </v-row>
    </v-container>

  </div>
</template>

<script>
import DataTable from "../components/DataTable";
import Renderer from "../components/Renderer.vue";

export default {
  name: "HomeView",

  components: {
    DataTable,
    Renderer,
  },

  data() {
    return {
      objectUrls: [],
      filter: [],
    };
  },
  methods: {
    setRenderer(url) {
      this.objectUrls = [url];
    },
    applyFilter(filter) {
      this.filter = filter;
    },
  }
};
</script>

<style>
.container {
  max-width: 100vw;
  padding: 10px;
}
</style>