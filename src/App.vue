<script setup lang="ts">
// for import components
</script>

<template>
  <header>
    <nav class="container">
      <a href="#">
        <img src="./assets/images/logo.svg" alt="Site Logo" />
      </a>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#" class="active">Order</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
      <div class="auth-options">
        <a href="#">Login</a>
        <a href="#" class="register-btn">Register</a>
      </div>
    </nav>
  </header>
  <div class="hero">
    <h1>Pizza Order</h1>
  </div>
  <main>
    <section class="pizza-options">
      <div>
        <h2>Choose your pizza</h2>
        <div class="pizza-types">
          <button>
            <div class="pizza-img">
              <img src="./assets/images/pizza/Cheese Pizza.png" alt="" />
            </div>
            <div class="pizza-price">
              <h3>Cheese Pizza</h3>
              <span>$8.00</span>
            </div>
          </button>
          <button>
            <div class="pizza-img">
              <img src="./assets/images/pizza/Veggie Pizza.png" alt="" />
            </div>
            <div class="pizza-price">
              <h3>Veggie Pizza</h3>
              <span>$8.50</span>
              <span class="price-disabled">$10.00</span>
            </div>
            <img class="ribbon-img" src="./assets/images/ribbon.svg" alt="" />
          </button>
          <button>
            <div class="pizza-img">
              <img src="./assets/images/pizza/Classical Pizza.png" alt="" />
            </div>
            <div class="pizza-price">
              <h3>Classical Pizza</h3>
              <span>$8.00</span>
            </div>
          </button>
        </div>
      </div>
      <div>
        <h2>Custom Pizza</h2>
        <h3>Size</h3>
        <div class="pizza-sizes">
          <div>
            <input id="small" type="radio" name="size" value="small" />
            <label for="small">Small</label>
          </div>
          <div>
            <input id="medium" type="radio" name="size" value="medium" />
            <label for="medium">Medium</label>
          </div>
          <div>
            <input id="large" type="radio" name="size" value="large" />
            <label for="large">Large</label>
          </div>
        </div>
      </div>
      <div>
        <h3>Toppings</h3>
        <div class="pizza-toppings">
          <button>Avocado</button>
          <button>Broccoli</button>
          <button class="active">Onions</button>
          <button disabled>Zucchini</button>
          <button>Lobster</button>
          <button>Oyster</button>
          <button>Salmon</button>
          <button>Tuna</button>
          <button>Bacoon</button>
          <button>Duck</button>
          <button>Ham</button>
          <button>Sausage</button>
        </div>
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
  <!-- <h1>{{ name }}</h1>
  <button @click="changeName('Zelda')">Change Name</button> -->
  <footer>
    <div class="container">
      <div class="find-us">
        <img class="logo" src="./assets/images/logo-alt.svg" alt="" />
        <div>
          <h3>Find Us :</h3>
          <div class="socmed">
            <a href="#">
              <img style="width: 10px" src="./assets/images/icons/facebook.svg" alt="" />
            </a>
            <a href="#">
              <img src="./assets/images/icons/instagram.svg" alt="" />
            </a>
            <a href="#">
              <img src="./assets/images/icons/youtube.svg" alt="" />
            </a>
          </div>
        </div>
      </div>
      <div class="navigation">
        <h3>Navigation</h3>
        <div>
          <a href="#">Home</a>
          <a href="#">Order</a>
          <a href="#">About</a>
          <a href="#">Blog</a>
          <a href="#">Contact</a>
          <a href="#">Login</a>
          <a href="#">Register</a>
        </div>
      </div>
      <div class="contact">
        <h3>Contact</h3>
        <div class="contact-list">
          <img src="./assets/images/icons/mail.svg" alt="" />
          <a href="mailto:food.now@mail.com"> Food.now@mail.com </a>
        </div>
        <div class="contact-list">
          <img src="./assets/images/icons/phone.svg" alt="" />
          <a href="tel:+62848477102943">+62848477102943</a>
        </div>
        <div class="contact-list">
          <img src="./assets/images/icons/whatsapp.svg" alt="" />
          <a href="https://wa.me/628184938494">+628184938494</a>
        </div>
      </div>
      <div class="location">
        <h3>Location</h3>
        <div class="location-title">
          <img src="./assets/images/icons/location.svg" alt="" />Kerobokan
        </div>
        <a href="#"
          >Jl. Raya Kerobokan Br Taman, Kuta No. 98, Kerobokan Kelod, Kec. Kuta Utara, Kabupaten
          Badung, Bali 80361
        </a>
      </div>
    </div>
    <div class="footer-credit">
      <div>
        Copyright &copy; 2022 Foodnow. All Rights Reserved. Powered by PT. Timedoor Indonesia. |
        Privacy Policy
      </div>
      <div class="recaptcha">
        This site is protected by reCAPTCHA and the Google Privacy Policy and Terms of Service
        apply.
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'App',
  components: {},
  data() {
    return {
      name: 'Link',
      age: 25 as number | string
    }
  },
  methods: {
    changeName(name: string) {
      this.name = name
    }
  }
})
</script>

<style scoped></style>
