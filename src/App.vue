<template>
  <post-form />
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
  methods: {},
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  background: rgb(207, 190, 190);
  padding: 20px;
}
</style>
