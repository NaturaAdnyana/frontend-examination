<script setup lang="ts">
import PizzaTypeButton from '@/components/PizzaTypeButton.vue'
</script>

<template>
  <div class="pizza-types">
    <PizzaTypeButton pizzaSrc="Cheese Pizza.png" title="Cheese Pizza" price="$8.00" />
    <PizzaTypeButton
      pizzaSrc="Veggie Pizza.png"
      title="Veggie Pizza"
      price="$8.50"
      oldPrice="$10.00"
      :offer="true"
    />
    <PizzaTypeButton pizzaSrc="Classical Pizza.png" title="Classical Pizza" price="$8.00" />
  </div>
</template>

<script lang="ts"></script>
