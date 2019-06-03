<template>
  <section>
    <nav-bar></nav-bar>
    <rockets class="container mt-3"></rockets>
  </section>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import Rockets from "@/views/Rockets.vue";
export default {
  name: "app",
  components: {
    NavBar,
    Rockets
  }
};
</script>

<style scoped>
</style>