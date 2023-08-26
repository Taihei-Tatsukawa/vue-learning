<script setup>
  import { computed, ref } from 'vue'
  import MyKyoto from './components/MyKyoto.vue'
  import MyTokyo from './components/MyTokyo.vue'

  const city = ref('tokyo')

  const tabs = {
    tokyo: MyTokyo,
    kyoto: MyKyoto,
  }
  const tab = computed(() => tabs[city.value])
</script>

<template>
  <h1>Vue！</h1>
  <div class="">
    <button
      class="flex bg-slate-200 text-2xl"
      @click="city = 'tokyo'"
    >
      東京
    </button>
    <button @click="city = 'kyoto'">京都</button>
  </div>
  <keep-alive>
    <component :is="tab"></component>
  </keep-alive>
  <my-kyoto></my-kyoto>
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
