<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input-custom
      v-model="post.title"
      placeholder="Название"
     />
    <input-custom 
      v-model="post.body"
      placeholder="Описание"
    />
   
    <!-- <button class="create" @click="createPost">Создать</button> -->
    <button-custom class="post-btn" @click="createPost">
      Создать
    </button-custom>
  </form>
</template>

<script>
import InputCustom from './UI/InputCustom.vue';
export default {
  components: { InputCustom },
  
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

.post-btn {
  align-self: center;
}

</style>