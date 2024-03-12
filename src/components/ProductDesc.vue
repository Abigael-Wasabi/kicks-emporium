<template>
  <section class="product-desc">
    <h2 style="text-align: center">At one's Disposal, Select Your Liking &#128525;</h2>
    <article class="sizes">
      <h3 style="text-align: center">Pick a Size</h3>
      <figure style="text-align: center">
        <button :class="{ active: active[0], btn: true }" @click="toggle(0)">7</button>
        <button :class="{ active: active[1], btn: true }" @click="toggle(1)">8</button>
        <button :class="{ active: active[2], btn: true }" @click="toggle(2)">9</button>
        <button :class="{ active: active[3], btn: true }" @click="toggle(3)">10</button>
        <button :class="{ active: active[4], btn: true }" @click="toggle(4)">11</button>
        <button :class="{ active: active[5], btn: true }" @click="toggle(5)">12</button>
      </figure>
    </article>
    <article class="quantity" style="justify-content: center">
      <button class="add" @click="increment">
        <img src="@/assets/images/plus.png" alt="plus-icon" />
      </button>
      <p>{{ count }}</p>
      <button class="minus" @click="decrement" :disabled="count === 0">
        <img src="../assets/images/minus.png" alt="minus-icon" />
      </button>
    </article>
    <article class="cart">
      <button @click="addToCart" style="margin: 0 auto" class="addToCart">Add To Cart</button><br>
    </article>
    <p style="margin: 0 auto; color:salmon" v-if="count > 0">
      <!-- <b>TOTAL: <span style="color:salmon">${{ total }}</span></b> -->
    </p>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import '@/assets/styles/ProductDesc.scss'

const productName = ref('')
const productPrice = ref(0)
const count = ref(0)
const active = ref([true, false, false, false, false, false])
let total = 0

function increment() {
  count.value++
  total = count.value * productPrice.value
}

function decrement() {
  if (count.value > 0) {
    count.value--
    total = count.value * productPrice.value
  }
}

function toggle(index) {
  active.value = active.value.map((value, i) => i === index)
}

function addToCart() {
  // Add logic to add the product to the cart
}
</script>



