<template>
  <section class="images">
    <section class="product-details">
      <h2>{{ productName }}</h2>
      <p>$ {{ productPrice }}</p>
    </section>
    <article class="main-images">
      <img v-if="active[0]" :src="thumb1" alt="purple" @click="toggleActive(0)" />
      <img v-if="active[1]" :src="thumb2" alt="blue" @click="toggleActive(1)" />
      <img v-if="active[2]" :src="thumb3" alt="red" @click="toggleActive(2)" />
      <img v-if="active[3]" :src="image1" alt="brown" @click="toggleActive(3)" />
      <img v-if="active[4]" :src="image2" alt="white" @click="toggleActive(4)" />
      <img v-if="active[5]" :src="image3" alt="black" @click="toggleActive(5)" />
      <img v-if="active[6]" :src="image4" alt="beige" @click="toggleActive(6)" />
      <img v-if="active[7]" :src="image5" alt="gray" @click="toggleActive(7)" />
      <img v-if="active[8]" :src="image6" alt="pink" @click="toggleActive(8)" />
      <img v-if="active[9]" :src="image7" alt="green" @click="toggleActive(9)" />
      <img v-if="active[10]" :src="image8" alt="yellow" @click="toggleActive(10)" />
      <img v-if="active[11]" :src="image9" alt="navy" @click="toggleActive(11)" />
      <img v-if="active[12]" :src="image10" alt="plain" @click="toggleActive(12)" />
      <img v-if="active[13]" :src="image11" alt="blunt" @click="toggleActive(13)" />
      <img v-if="active[14]" :src="image12" alt="mahon" @click="toggleActive(14)" />
    </article>
    <article class="thumbnails">
      <img :src="thumb1" :class="{ active: active[0], thumbnail: true }" @click="toggleActive(0)" alt="purple" />
      <img :src="thumb2" :class="{ active: active[1], thumbnail: true }" @click="toggleActive(1)" alt="blue" />
      <img :src="thumb3" :class="{ active: active[2], thumbnail: true }" @click="toggleActive(2)" alt="red" />
      <img :src="image1" :class="{ active: active[3], thumbnail: true }" @click="toggleActive(3)" alt="brown" />
      <img :src="image2" :class="{ active: active[4], thumbnail: true }" @click="toggleActive(4)" alt="white" />
      <img :src="image3" :class="{ active: active[5], thumbnail: true }" @click="toggleActive(5)" alt="black"  />
      <img :src="image4" :class="{ active: active[6], thumbnail: true }" @click="toggleActive(6)" alt="beige" />
      <img :src="image5" :class="{ active: active[7], thumbnail: true }" @click="toggleActive(7)" alt="gray" />
      <img :src="image6" :class="{ active: active[8], thumbnail: true }" @click="toggleActive(8)" alt="pink" />
      <img :src="image7" :class="{ active: active[9], thumbnail: true }" @click="toggleActive(9)" alt="green" />
      <img :src="image8" :class="{ active: active[10], thumbnail: true }" @click="toggleActive(10)" alt="yellow" />
      <img :src="image9" :class="{ active: active[11], thumbnail: true }" @click="toggleActive(11)" alt="navy" />
      <img :src="image10" :class="{ active: active[12], thumbnail: true }" @click="toggleActive(12)" alt="plain" />
      <img :src="image11" :class="{ active: active[13], thumbnail: true }" @click="toggleActive(13)" alt="blunt" />
      <img :src="image12" :class="{ active: active[14], thumbnail: true }" @click="toggleActive(14)" alt="mahon"  />
    </article>
  </section>
</template>

<script setup>
import '@/assets/styles/ProductImages.scss'
import thumb1 from '@/assets/images/purple.jpg'
import thumb2 from '@/assets/images/blue.jpg'
import thumb3 from '@/assets/images/red.jpg'
import image1 from '@/assets/images/brown.jpg'
import image2 from '@/assets/images/white.jpg'
import image3 from '@/assets/images/black.jpg'
import image4 from '@/assets/images/beige.jpg'
import image5 from '@/assets/images/gray.jpg'
import image6 from '@/assets/images/pink.jpg'
import image7 from '@/assets/images/green.jpg'
import image8 from '@/assets/images/yellow.jpg'
import image9 from '@/assets/images/navy.jpg'
import image10 from '@/assets/images/plain.jpg'
import image11 from '@/assets/images/blunt.jpg'
import image12 from '@/assets/images/mahon.jpg'
import { ref } from 'vue'

const productName = ref('')
const productPrice = ref(0)
const active = ref(Array(15).fill(false))

function toggleActive(index) {
  active.value = active.value.map((value, i) => i === index)
  switch (index) {
    case 0:
      productName.value = 'bullets'
      productPrice.value = 200
      break
    case 1:
      productName.value = 'converse'
      productPrice.value = 250
      break
    case 2:
      productName.value = 'denim'
      productPrice.value = 300
      break
    case 3:
      productName.value = 'J1'
      productPrice.value = 400
      break
    case 4:
      productName.value = 'bata'
      productPrice.value = 500
      break
    case 5:
      productName.value = 'rubbers'
      productPrice.value = 600
      break
    case 6:
      productName.value = 'boots'
      productPrice.value = 700
      break
    case 7:
      productName.value = 'ankle'
      productPrice.value = 800
      break
    case 8:
      productName.value = 'drip'
      productPrice.value = 900
      break
    case 9:
      productName.value = 'level'
      productPrice.value = 1000
      break
    case 10:
      productName.value = 'timber'
      productPrice.value = 1100
      break
    case 11:
      productName.value = 'buffalo'
      productPrice.value = 1200
      break
    case 12:
      productName.value = 'genie'
      productPrice.value = 1300
      break
    case 13:
      productName.value = 'finla'
      productPrice.value = 3200
      break
    case 14:
      productName.value = 'prey'
      productPrice.value = 2300
      break
    default:
      break
  }
}
</script>

<style scoped>
.product-details {
  color: orangered;
  margin-top: 10px;
}
</style>
