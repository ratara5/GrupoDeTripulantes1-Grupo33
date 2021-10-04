<template>
  <BasicLayouts>
    <h2>Aquí va el Home</h2>
    <Testimonios />
  </BasicLayouts>
</template>

<script>
// @ is an alias to /src
import BasicLayouts from "../layouts/BasicLayouts.vue";
import Testimonios from "../components/Testimonios.vue"
export default {
  name: "Home",
  components: {
    BasicLayouts,
    Testimonios,
  },
};
</script>
