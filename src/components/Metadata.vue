<template>
  <div>
    <h3>Metadatos</h3>
    <p v-if="layer">Fuente: {{ metadata[layer].fuente }}</p>
    <p v-if="layer">Fecha: {{ metadata[layer].fecha }}</p>
  </div>
</template>

<script>
export default {
  name: 'Metadata',
  props: ['layer'],
  data() {
    return {
      metadata: {
        clima: { fuente: 'IDEAM', fecha: '2026-02-11' },
        hidrologia: { fuente: 'Copernicus', fecha: '2026-02-11' }
      }
    };
  }
};
</script>

