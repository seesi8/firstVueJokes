<template>
  <div class="container">
    <AppHeader />
    <Nuxt />
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader.vue";
export default {
  components: {
    AppHeader,
  },
};
</script>

<style>
body {
  margin: 0;
  background-color: rgb(218, 212, 212);
}
</style>
