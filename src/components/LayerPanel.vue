<template>
  <div>
    <h3>Capas disponibles</h3>
    <label><input type="checkbox" v-model="layers.clima" @change="toggleLayer('clima')"> Clima</label>
    <label><input type="checkbox" v-model="layers.hidrologia" @change="toggleLayer('hidrologia')"> Hidrología</label>
  </div>
</template>

<script>
export default {
  name: 'LayerPanel',
  data() {
    return {
      layers: { clima: false, hidrologia: false }
    };
  },
  methods: {
    toggleLayer(layer) {
      this.$emit('toggle-layer', layer, this.layers[layer]);
    }
  }
};
</script>

