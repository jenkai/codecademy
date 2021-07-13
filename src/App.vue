<template>
  <Navbar />
  <Page-1 />
</template>

<script>
import Navbar from "./components/Navbar/Navbar.vue";
import Page1 from "./components/Page1.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Page1,
  },
};
</script>

<style>
#app {
  font-family: Apercu;
  color: #10162f;
}

body {
  margin: 0%;
}

* {
  box-sizing: border-box;
}
</style>
