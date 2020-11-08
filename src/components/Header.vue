<template>
  <header>
    <h1 v-on:click="changeTitle">{{ title }}</h1>
  </header>
</template>

<script>
// import { bus } from "../main";

export default {
  props: {
    title: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      //   title: "Vue",
    };
  },
  methods: {
    changeTitle: function() {
        this.$emit("changeTitleParent", "Vue wizards");
    //   this.title = "Vue wizards";
    //   bus.$emit("titleChanged", "Vue wizards");
    },
  },
};
</script>

<style scoped>
header {
  background: lightgreen;
  padding: 10px;
}
h1 {
  color: #222;
  text-align: center;
}
</style>
