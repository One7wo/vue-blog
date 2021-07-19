<template>
<div class="post">
      <div>

        <div><strong>Название:</strong> {{ post.title }}</div>
        <div><strong>Описание:</strong> {{ post.body }}</div>

      </div>
    <button-custom class="post-btn-del" @click="$emit('remove', post)">
        Удалить
    </button-custom>
</div>
  
</template>

<script>
export default {
   
    props: {
        post: {
            type: Object,
            required: true
        }
    }
}
</script>

<style>
.post {
  padding: 15px;
  background: #ffffff;
  border-radius: 8px;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.post:last-child {
  margin-bottom: 0px;
}


</style>