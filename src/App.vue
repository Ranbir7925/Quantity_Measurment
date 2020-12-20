<template>
  <div id="app">
    <AppBar />
    <Conversion />
  </div>
</template>

<script>
import AppBar from "./components/AppBar";
import Conversion from "./components/Conversion";
export default {
  name: "app",
  components: {
    AppBar,
    Conversion,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
body {
  background-color: #f4f5f7;
}
#app {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
