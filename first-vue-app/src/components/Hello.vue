<script setup>
const { message, name } = defineProps({
  message: String,
  name: {
    type: String,
    default: 'Fuga',
  },
});
</script>

<template>
  <h2>fist component</h2>
  <p>{{ message }}</p>
  <p>{{ name }}</p>
</template>
