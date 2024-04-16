<template>
  <v-card>
    <v-card-text>
      <div class="d-flex align-center">
        <span class="mr-5">Sun shadows</span>
        <v-switch v-model="settings.enabled" inset :label="``" />
      </div>
      <v-slider
        v-model="settings.intensity"
        step="0"
        max="10"
        min="1"
        :thumb-size="24"
        label="Sun intensity"
        :disabled="!settings.enabled"
      />
      <v-slider
        v-model="settings.elevation"
        step="0"
        :min="0"
        :max="Math.PI"
        :thumb-size="24"
        label="Sun elevation"
        :disabled="!settings.enabled"
      />
      <v-slider
        v-model="settings.azimuth"
        step="0"
        :min="-Math.PI * 0.5"
        :max="Math.PI * 0.5"
        :thumb-size="24"
        label="Sun azimuth"
        :disabled="!settings.enabled"
      />
      <v-slider
        v-model="settings.indirectLightIntensity"
        step="0"
        min="0.0"
        max="5.0"
        :thumb-size="24"
        label="Indirect light"
      />
    </v-card-text>
  </v-card>
</template>
<script lang="ts">
export default {
  name: "RendererLightingOptions",
  props: {
    value: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      settings: this.value,
    };
  },
  watch: {
    settings: {
      handler() {
        this.$emit("input", this.settings);
      },
      deep: true,
    },
  },
};
</script>
