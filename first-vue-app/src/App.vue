<script setup>
const users = [
  { id: 1, name: 'John Doe', email: 'john@test.com', admin: true },
  { id: 2, name: 'Jane Doe', email: 'jane@example.com', admin: false },
  { id: 3, name: 'Kevin MacDonald', email: 'kevin@test.com', admin: false },
];
</script>

<template>
  <h1>Vue 入門</h1>
  <div v-for="user in users" :key="user.id">
    <div v-if="!user.admin">
      <ul>
        <li v-for="(value, name) in user" :key="value">{{ name }}:{{ value }}</li>
      </ul>
    </div>
  </div>
</template>

<style></style>
