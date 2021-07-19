<template>
  <h1>Страница с постами</h1>
  <button-custom @click="showModal" class="post-btn" style="margin-top: 20px;">Создать пост</button-custom>
  <create-post v-model:show="modalVisible">
    <post-form  @create="createPost" />
  </create-post>
  <post-list :posts="posts" @remove="removePost" />
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
      modalVisible: false
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
      this.modalVisible = false
    },
    removePost(post) {
      this.posts = this.posts.filter( p => p.id !== post.id)
    },
    showModal() {
      this.modalVisible = true
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
