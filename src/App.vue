<template>
  <post-form  @create="createPost" />
  <post-list :posts="posts" />
</template>

<script>
import PostList from "./components/PostList";
import PostForm from "./components/PostForm";
export default {
  components: {
    PostList,
    PostForm,
  },
  data() {
    return {
      posts: [],
      title: "",
      body: "",
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
    }
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  background: #e2e2e2;
  padding: 20px;
}
</style>
