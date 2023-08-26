<template>
  <div>
    <h2>CompAコンポーネント</h2>
    <p>CompAのcount: {{ counter.count }}</p>
    <CompB :message="message" />
  </div>
</template>

<script setup>
  import { counter } from '../store/countStore'
  import CompB from './CompB.vue'

  const { message } = defineProps({
    message: {
      type: String,
      required: true,
    },
  })
</script>

<style lang="scss" scoped></style>
