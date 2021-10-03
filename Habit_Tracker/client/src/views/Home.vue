<template>
  <BasicLayouts>
    <h2>Aquí va el Home</h2>
    <h3>Lo demás puede manejarse como componentes</h3>
  </BasicLayouts>
</template>

<script>
// @ is an alias to /src
import BasicLayouts from "../layouts/BasicLayouts.vue";
export default {
  name: "Home",
  components: {
    BasicLayouts,
  },
};
</script>
