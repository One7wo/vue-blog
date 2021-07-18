<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input
      v-model="post.title"
      class="input"
      type="text"
      placeholder="Название"
    />
    <input
      v-model="post.body"
      class="input"
      type="text"
      placeholder="Описание"
    />
    <button class="create" @click="createPost">Создать</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit('create', this.post)
      this.post = {
      title: "",
      body: ""
      }
      
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}
form h4 {
  margin-bottom: 10px;
}
.input {
  padding: 15px 10px;
  border-radius: 8px;
  background: #fff;
  outline: none;
  border: none;
  margin-bottom: 10px;
}
.create {
  background: #fff;
  color: #6ea36e;
  font-weight: bold;
  padding: 10px;
  width: 150px;
  outline: none;
  border: 1px solid #6ea36e;
  border-radius: 8px;
  cursor: pointer;
  /* margin: 0 auto; */
  align-self: flex-end;
}
.create:hover {
  background: #6ea36e;
  font-weight: bold;
  color: #fff;
  border: 1px solid #6ea36e;
}
</style>