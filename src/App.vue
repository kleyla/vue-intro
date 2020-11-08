<template>
  <div id="app">
    <app-header></app-header>
    <Friends></Friends>
    <app-footer></app-footer>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer";
import Friends from "./components/Friends";

export default {
  name: "App",
  components: {
    // HelloWorld,
    "app-header": Header,
    "app-footer": Footer,
    Friends,
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
}
</style>
