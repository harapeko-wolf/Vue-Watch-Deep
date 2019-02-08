<template>
  <div id="app"><WatchDeep /></div>
</template>

<script>
import WatchDeep from "./components/WatchDeep";

export default {
  name: "App",
  components: {
    WatchDeep
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
