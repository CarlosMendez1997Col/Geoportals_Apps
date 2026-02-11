<template>
  <div id="map" style="height:500px; width:100%;"></div>
</template>

<script>
import L from 'leaflet';

export default {
  name: 'MapView',
  mounted() {
    const map = L.map('map').setView([4.711, -74.072], 6); // Bogotá
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '© OpenStreetMap contributors'
    }).addTo(map);
  }
};
</script>

