<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar />
  </div>
</template>

<script>
import Navbar from "./Navbar";
export default {
  name: "app",
  components: {
    Navbar,
  },
  data() {
    return {
      title: "Smell My Hair Daddy Joe ;)",
    };
  },
};
</script>

<style>
h1 {
  color: red;
  font-weight: normal;
  text-align: center;
}
</style>
