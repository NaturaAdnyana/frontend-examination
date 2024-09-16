<script setup lang="ts">
import { PropType } from 'vue'

interface Size {
  id: number
  name: string
  extra_price: number
}

const props = defineProps({
  sizes: {
    type: Array as PropType<Size[]>,
    required: true
  }
})
</script>

<template>
  <div class="pizza-sizes">
    <div v-for="size in sizes" :key="size.id">
      <input
        :id="size.name.toLowerCase()"
        type="radio"
        name="size"
        :value="size.name.toLowerCase()"
      />
      <label :for="size.name.toLowerCase()">{{ size.name }}</label>
      <span v-if="size.extra_price > 0">(+{{ size.extra_price }}$)</span>
    </div>
  </div>
</template>
