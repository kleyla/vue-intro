<template>
  <div id="mi-componente">
    <h1>Este es mi componente</h1>
    <h2>{{ subtitulo }}</h2>
    <p>{{ greeting() }}</p>
    <ul>
      <li v-for="(girl, index) in girls" v-bind:key="index">{{ girl }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MiComponente",
  data() {
    return {
      subtitulo: "Soy el subtitulo",
      girls: ["Karen", "yol", "andy"],
    };
  },
  methods: {
    greeting: function() {
      return "hi!";
    },
  },
};
</script>
<style scoped>
h1 {
  color: red;
}
</style>
