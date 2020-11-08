<template>
  <div>
    <addBlog></addBlog>
  </div>
</template>

<script>
import addBlog from "./components/addBlog";

export default {
  name: "App",
  components: {
    addBlog,
  },
  data() {
    return {
      title: "Vue js",
    };
  },
  methods: {},
};
</script>

<style>
body {
  margin: 0;
  font-family: "Nunito Semibold";
}
</style>
