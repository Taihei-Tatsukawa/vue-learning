<template>
  <div>
    <h3>CompBコンポーネント</h3>
    <p>{{ message }}</p>
    <p>{{ message2 }}</p>
    <p>Count: {{ counter.count }}</p>
    <button @click="counter.addCount">count up</button>
  </div>
</template>

<script setup>
  import { inject } from 'vue'
  import { counter } from '../store/countStore'

  const { message } = defineProps({
    message: {
      type: String,
      required: true,
    },
  })

  const message2 = inject('message')
</script>

<style lang="scss" scoped></style>
