<template>
  <button>
    <div class="pizza-img">
      <img :src="getImageUrl(pizzaSrc)" alt="" />
    </div>
    <div class="pizza-price">
      <h3>{{ title }}</h3>
      <span>{{ price }}</span>
      <span v-if="oldPrice" class="price-disabled">{{ oldPrice }}</span>
    </div>
    <img v-if="offer" class="ribbon-img" src="../assets/images/ribbon.svg" alt="" />
  </button>
</template>

<script setup>
const getImageUrl = (name) => {
  return new URL(`../assets/images/pizza/${name}`, import.meta.url).href
}
const props = defineProps({
  pizzaSrc: String,
  title: String,
  price: String,
  oldPrice: String,
  offer: Boolean
})
</script>
