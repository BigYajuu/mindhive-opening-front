<script>
import Map from './components/Map.vue';
import '../node_modules/mapbox-gl/dist/mapbox-gl.css';

export default {
  components: {
    Map,
  },

  data: () => ({
    location: {
      lng: 101.6841,
      lat: 3.1319,
      bearing: 0,
      pitch: 0,
      zoom: 11,
    },
  }),
};
</script>

<template>
  <div id="layout">
    <div id="sidebar">
      Chickenlist1,<br />
      Chickenlist1, Chickenlist1
    </div>
    <Map v-model="location" />
  </div>
</template>

<style>
#layout {
  flex: 1;
  display: flex;
}

#sidebar {
  background-color: rgb(35 55 75 / 90%);
  color: #fff;
  padding: 6px 12px;
  font-family: Helvetica;
  z-index: 1;
  position: absolute;
  bottom: 0;
  left: 0;
  margin: 12px;
  border-radius: 4px;
}
</style>
