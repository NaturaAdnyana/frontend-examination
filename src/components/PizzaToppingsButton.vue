<template>
  <button :class="{ active: activeTopping }" :disabled="disabledTopping">
    {{ name }}
  </button>
</template>

<script setup lang="ts">
const props = defineProps({
  name: {
    type: String,
    required: true
  },
  activeTopping: {
    type: Boolean,
    default: false
  },
  disabledTopping: {
    type: Boolean,
    default: false
  }
})
</script>
