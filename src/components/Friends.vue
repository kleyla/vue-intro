<template>
  <div id="friends">
    <ul>
      <li
        v-for="(friend, index) in friends"
        :key="index"
        v-on:click="friend.show = !friend.show"
      >
        <h2>{{ friend.name }}</h2>
        <h3 v-show="friend.show">{{ friend.speciality }}</h3>
      </li>
    </ul>
    <button v-on:click="deleteFriend">Delete friend</button>
  </div>
</template>

<script>
export default {
  props: {
    friends: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {};
  },
  methods: {
    deleteFriend: function() {
      this.friends.pop();
    },
  },
  // beforeCreate() {
  //   alert("Before create!");
  // },
  // created() {
  //   alert("Created!");
  // },
  // beforeMount() {
  //   alert("Before Mount");
  // },
  // mounted() {
  //   alert("Mounted");
  // },
  // beforeUpdate() {
  //   alert("Before update");
  // },
  // updated() {
  //   alert("updated");
  // },
};
</script>

<style scoped>
#friends {
  width: 100%;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
  box-sizing: border-box;
}
ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}
li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 30px;
  border: 1px solid #222;
  margin: 10px;
}
</style>
