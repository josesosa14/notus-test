<template>
  <section>
  <GoogleMapLoader
    :configMap="configMap"
    :apiKey="configMap.apiKey"
  >
    <template slot-scope="{ google, map }">
      <GoogleMapMaker
        v-for="marker in markers"
        :key="marker.id"
        :marker="marker"
        :google="google"
        :map="map"
      />
    </template>
  </GoogleMapLoader>
  </section>
</template>

<script>

  import GoogleMapLoader from "./GoogleMapLoader";
  import GoogleMapMaker from "./GoogleMapMaker";
  import { configMap } from "@/constants/configMap";


  export default {
    components: {
      GoogleMapLoader,
      GoogleMapMaker
    },

    data() {
      return {
        markers: [
          {
            id: "0",
            position: { lat: 45.7874971, lng: 16.0283393 },
            title: "Notus"
          }
        ]
      };
    },

    computed: {
      configMap() {
        return {
          ...configMap,
          center: this.mapCenter
        };
      },

      mapCenter() {
        return this.markers[0].position;
      }
    }
  };
  
</script>
<style>
  div .map{
    margin: 0 auto;
  }
</style>