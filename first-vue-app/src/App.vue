<template>
  <div>
    <h1>Vue3 入門</h1>
    <CompA message="propsでデータ渡し" />
    <input
      type="text"
      :value="message"
      @input="message = $event.target.value"
    />
  </div>
</template>

<script setup>
  import { provide, ref } from 'vue'
  import CompA from './components/CompA.vue'
  const message = ref('Provide/Injectでデータ渡し')

  const count = ref(0)

  const addCount = () => {
    count.value++
  }

  provide('message', message)
  provide('count', {
    count,
    addCount,
  })
</script>

<style lang="scss" scoped></style>
