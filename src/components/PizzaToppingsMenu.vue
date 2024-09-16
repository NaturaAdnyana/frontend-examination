<template>
  <div class="pizza-toppings">
    <div v-for="topping in toppings" :key="topping.id">
      <PizzaToppingsButton :name="topping.name" :activeTopping="false" :disabledTopping="false" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { PropType } from 'vue'
import PizzaToppingsButton from './PizzaToppingsButton.vue'

interface Topping {
  id: number
  name: string
  price: number
}

const props = defineProps({
  toppings: {
    type: Array as PropType<Topping[]>,
    required: true
  }
})
</script>
