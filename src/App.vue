<template>
  <div id="app">
    <VerticalList />
  </div>
</template>

<script>
import VerticalList from "./components/VerticalList.vue";

export default {
  name: "App",
  components: {
    VerticalList,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin-left: 10vh;
  margin-right: 10vh;
}
</style>
