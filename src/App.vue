<script setup lang="ts">
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import FooterSection from './components/FooterSection.vue'
import PizzaTypesMenu from './components/PizzaTypesMenu.vue'
import PizzaSizesMenu from './components/PizzaSizesMenu.vue'
import PizzaToppingsMenu from './components/PizzaToppingsMenu.vue'

import sizes from './assets/data/json/size-list.json'
import toppings from './assets/data/json/topping-list.json'
import pizzaList from './assets/data/json/pizza-list.json'
</script>

<template>
  <header>
    <NavBar />
  </header>
  <HeroSection />
  <main>
    <section class="pizza-options">
      <div>
        <h2>Choose your pizza</h2>
        <PizzaTypesMenu :pizzaTypes="pizzaList.data" />
      </div>
      <div>
        <h2>Custom Pizza</h2>
        <h3>Size</h3>
        <PizzaSizesMenu :sizes="sizes.data" />
      </div>
      <div>
        <h3>Toppings</h3>
        <PizzaToppingsMenu :toppings="toppings.data" />
      </div>
    </section>
    <aside>
      <div>
        <h2>Payment Summary</h2>
        <table>
          <tbody>
            <tr>
              <td width="50%">Veggie Pizza</td>
              <td width="50%">8$</td>
            </tr>
            <tr>
              <td width="50%">Veggie Pizza</td>
              <td width="50%">8$</td>
            </tr>
          </tbody>
        </table>
        <div class="count-total">
          <hr class="divider" />
          <div>
            <span>Total Price</span>
            <span class="total-price">$12.00</span>
          </div>
          <button>Order Now</button>
        </div>
      </div>
    </aside>
  </main>
  <FooterSection />
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'App'
})
</script>

<style scoped></style>
