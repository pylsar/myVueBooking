<template>
  <div class="googlemap">
    <gmap-map v-bind="options" id="map"> </gmap-map>
  </div>
</template>

<script>
import { gmapApi } from "vue2-google-maps";
export default {
  name: "Googlemap",
  data() {
    return {
      options: {
        zoom: 10,
        center: {
          lat: 39.9995601,
          lng: -75.1395161,
        },
        mapTypeId: "roadmap",
      },
    };
  },
  computed: {
    google: gmapApi,
  },
};
</script>

<style lang="scss">
#map {
    width: 350px;
    height: 210px;
}
</style>
