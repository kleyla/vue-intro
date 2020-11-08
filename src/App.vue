<template>
  <div>
    <app-header
      v-bind:title="title"
      v-on:changeTitleParent="upadateTitle($event)"
    ></app-header>
    <keep-alive>
      <component v-bind:is="component"></component>
    </keep-alive>
    <button v-on:click="component = 'formOne'">Show form one</button>
    <button v-on:click="component = 'formTwo'">Show form two</button>
    <Friends v-bind:friends="friends"></Friends>
    <Friends v-bind:friends="friends"></Friends>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer";
import Friends from "./components/Friends";
// import formHelper from "./components/formHelper.vue";
import formOne from "./components/formOne";
import formTwo from "./components/formTwo";

export default {
  name: "App",
  components: {
    // HelloWorld,
    "app-header": Header,
    "app-footer": Footer,
    Friends,
    // formHelper,
    formOne,
    formTwo,
  },
  data() {
    return {
      friends: [
        { name: "Andrea", speciality: "React js", show: false },
        { name: "Rocio", speciality: "Laravel js", show: false },
        { name: "Yol", speciality: "Angular js", show: false },
        { name: "Daniel", speciality: "React js", show: false },
        { name: "Juan", speciality: "Vue js", show: false },
      ],
      title: "Vue js",
      component: "formOne",
    };
  },
  methods: {
    upadateTitle: function(updatedTitle) {
      this.title = updatedTitle;
    },
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
}
</style>
