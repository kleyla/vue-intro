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
  </div>
</template>

<script>
export default {
    data() {
        return {
            friends: [
                {name: 'Andrea', speciality:"React js", show: false},
                {name: 'Rocio', speciality:"Laravel js", show: false},
                {name: 'Yol', speciality:"Angular js", show: false},
                {name: 'Daniel', speciality:"React js", show: false},
                {name: 'Juan', speciality:"Vue js", show: false},
            ]
        }
    },
}
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
