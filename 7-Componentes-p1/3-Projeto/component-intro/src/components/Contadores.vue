<template>
  <div class="contadores">
    <app-contador v-for="c in 10" :key="c"></app-contador>
  </div>
</template>

<script>
import Contador from "./Contador.vue";
export default {
  components: {
    "app-contador": Contador,
  },
};
</script>
<style></style>
