<script setup lang="ts">
import PizzaTypeButton from '@/components/PizzaTypeButton.vue'
import { PropType } from 'vue'

interface PizzaType {
  id: number
  name: string
  price: number
  discount: {
    is_active: boolean
    final_price: number
  }
  toppings: number[]
}

const props = defineProps({
  pizzaTypes: {
    type: Array as PropType<PizzaType[]>,
    required: true
  }
})
</script>

<template>
  <div class="pizza-types">
    <div v-for="type in pizzaTypes" :key="type.id">
      <PizzaTypeButton
        :pizzaSrc="`${type.name}.png`"
        :title="type.name"
        :price="`$${type.discount.is_active ? type.discount.final_price : type.price}`"
        :oldPrice="type.discount.is_active ? `$${type.price}` : ''"
        :offer="type.discount.is_active"
      />
    </div>
  </div>
</template>
