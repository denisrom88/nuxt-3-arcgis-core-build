<template>
  <div id="viewDiv"></div>
</template>

<script setup lang="ts">
import Map from "@arcgis/core/Map.js";
import MapView from "@arcgis/core/views/MapView.js";

onMounted(() => {
  const map = new Map({
    basemap: "topo-vector"
  });

  new MapView({
    container: "viewDiv",
    map: map,
    zoom: 4,
    center: [15, 65]
  });
});
</script>

<style>
@import url('https://js.arcgis.com/4.29/@arcgis/core/assets/esri/themes/light/main.css');

html, body, #__nuxt, #viewDiv {
  height: 100%;
  margin: 0;
}
</style>