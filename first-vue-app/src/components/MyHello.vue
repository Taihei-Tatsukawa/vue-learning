<script setup>
  import { ref } from 'vue'

  const props = defineProps({
    name: {
      type: String,
      required: true,
    },
  })

  // eslint-disable-next-line vue/no-setup-props-destructure
  const name = ref(props.name)

  const emit = defineEmits({
    changeNameEvent: (name) => {
      console.log(name)
      if (name) return true
      return false
    },
  })

  const changeName = () => {
    emit('changeNameEvent', name.value)
  }
</script>

<template>
  <h2>子コンポーネント</h2>
  <p>Hello {{ props.name }}</p>
  <input
    v-model="name"
    type="text"
    @input="changeName"
  />
</template>
