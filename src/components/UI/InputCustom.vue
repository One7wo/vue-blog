<template>
  <input class="input" type="text" :value="modelValue" @input="updateInput">
</template>

<script>
export default {
    name: 'input-custom',
    props: {
        modelValue: [String, Number]
    },
    methods: {
        updateInput(e) {
            this.$emit('update:modelValue', e.target.value)
        }
    }
}
</script>

<style>
.input {
  padding: 15px 10px;
  border-radius: 8px;
  background: #fff;
  outline: none;
  border: none;
  margin-bottom: 10px;
}
</style>