<template>
  <div>
    <addBlog></addBlog>
    <showBlogs></showBlogs>
    <hr />
    <listBlogs></listBlogs>
  </div>
</template>

<script>
import addBlog from "./components/addBlog";
import showBlogs from "./components/showBlogs.vue";
import listBlogs from "./components/listBlogs.vue";

export default {
  name: "App",
  components: {
    addBlog,
    showBlogs,
    listBlogs,
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
