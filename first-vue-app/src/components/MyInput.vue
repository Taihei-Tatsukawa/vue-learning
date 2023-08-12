<script setup>
  const props = defineProps({
    modelValue: {
      type: String,
      required: true,
    },
  })

  const emit = defineEmits(['update:modelValue'])
</script>

<template>
  <input
    :value="props.modelValue"
    style="padding: 1em; border-radius: 1em; margin: 0.5em"
    @input="emit('update:modelValue', $event.target.value)"
  />
</template>
