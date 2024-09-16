<template>
  <button>
    <div class="pizza-img">
      <img :src="getImageUrl(pizzaSrc)" alt="Pizza Image" />
    </div>
    <div class="pizza-price">
      <h3>{{ title }}</h3>
      <span>{{ price }}</span>
      <span v-if="oldPrice" class="price-disabled">{{ oldPrice }}</span>
    </div>
    <img v-if="offer" class="ribbon-img" src="../assets/images/ribbon.svg" alt="Special Offer" />
  </button>
</template>

<script setup lang="ts">
const getImageUrl = (name: string) => {
  return new URL(`../assets/images/pizza/${name}`, import.meta.url).href
}

const props = defineProps({
  pizzaSrc: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  price: {
    type: String,
    required: true
  },
  oldPrice: {
    type: String,
    default: null
  },
  offer: {
    type: Boolean,
    default: false
  }
})
</script>
