<script setup>
  import { ref } from 'vue'
  import MyHello from './components/MyHello.vue'
  import MyInput from './components/MyInput.vue'

  const helloName = ref('Vue')
  const name = ref('John Doe')
  const address = ref('')
</script>

<template>
  <h1>Vue！</h1>
  <MyHello
    :name="helloName"
    @change-name-event="helloName = $event"
  />
  <p>name: {{ name }}</p>
  <p>address: {{ address }}</p>
  <MyInput v-model="name" />
  <MyInput v-model="address" />
</template>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #7c828a;
    margin-top: 60px;
  }
</style>
