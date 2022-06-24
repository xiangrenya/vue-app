<template>
  <div id="amap"></div>
</template>

<script>
import "leaflet/dist/leaflet.css";
import L from "leaflet";

export default {
  name: "AMap",
  mounted() {
    const map = L.map("amap");

    L.tileLayer(
      "http://webrd01.is.autonavi.com/appmaptile?x={x}&y={y}&z={z}&lang=zh_cn&size=1&scale=1&style=8",
      {
        maxZoom: 24,
      }
    ).addTo(map);

    map.setView([31.369328, 120.504931], 14);
  },
};
</script>

<style lang="scss">
#amap {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
}
</style>
