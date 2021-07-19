<template>
  <button >
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'button-custom'
}
</script>

<style scoped>
.post-btn {
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
}
.post-btn:hover {
  background: #6ea36e;
  color: #fff;
  border: 1px solid #6ea36e;
}

.post-btn-del{
  background: #fff;
  color: #c96159;
  font-weight: bold;
  padding: 10px;
  outline: none;
  border-radius: 8px;
  cursor: pointer;
    width: 80px;
    border: 1px solid #c96159;
}
.post-btn-del:hover{
  background: #c96159;
  color: #fff;
  border: 1px solid #c96159;
}
</style>