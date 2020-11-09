<template>
  <div v-theme:column="'narrow'" id="show-blogs">
    <h1>All Blog Articles</h1>
    <input type="text" v-model="search" placeholder="search blogs" />
    <div
      class="single-blog"
      v-for="(blog, index) in filterdBlogs"
      v-bind:key="index"
    >
      <router-link v-bind:to="'/blog/' + blog.id">
        <h2 v-rainbow>{{ blog.title | toUppercase }}</h2></router-link
      >
      <article>{{ blog.content | snipped }}</article>
    </div>
  </div>
</template>

<script>
import searchMixin from "./../mixins/searchMixin.js";

export default {
  data() {
    return {
      blogs: [],
      search: "",
    };
  },
  created() {
    this.$http
      .get("https://vue-app-d4e37.firebaseio.com/post.json")
      .then(function(data) {
        // console.log(data.json());
        // this.blogs = data.body.slice(0, 10);
        return data.json();
      })
      .then(function(data) {
        var blogsArray = [];
        for (let key in data) {
          // console.log(key);
          // console.log(data[key]);
          data[key].id = key;
          blogsArray.push(data[key]);
        }
        // console.log(blogsArray);
        this.blogs = blogsArray;
      });
  },
  computed: {
    // filterdBlogs: function() {
    //   return this.blogs.filter((blog) => {
    //     return blog.title.match(this.search);
    //   });
    // },
  },
  //   filter locally
  filters: {
    toUppercase: function(value) {
      return value.toUpperCase();
    },
  },
  directives: {
    rainbow: {
      bind(el) {
        el.style.color =
          "#" +
          Math.random()
            .toString()
            .slice(2, 8);
      },
    },
  },
  mixins: [searchMixin],
};
</script>

<style scoped>
#show-blogs {
  max-width: 800px;
  margin: 0 auto;
}
.single-blog {
  padding: 20px;
  margin: 20px 0;
  box-sizing: border-box;
  background: #eee;
}
</style>
