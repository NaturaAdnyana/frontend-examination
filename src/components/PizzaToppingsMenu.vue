<template>
  <div class="pizza-toppings">
    <button
      v-for="(topping, index) in toppings"
      :key="index"
      :class="{ active: topping === activeTopping }"
      :disabled="topping === disabledTopping"
    >
      {{ topping }}
    </button>
  </div>
</template>

<script setup>
const props = defineProps({
  activeTopping: String,
  disabledTopping: String
})

// Example toppings array
const toppings = [
  'Avocado',
  'Broccoli',
  'Onions',
  'Zucchini',
  'Lobster',
  'Oyster',
  'Salmon',
  'Tuna',
  'Bacoon',
  'Duck',
  'Ham',
  'Sausage'
]
</script>
