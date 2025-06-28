<template>
  <q-page class="q-pa-md">
    <!-- Judul -->
    <div class="text-center q-mt-lg">
      <h1 class="text-primary text-h2">Enjoy Your Shopping</h1>
    </div>
    <!-- Carousel -->
    <q-carousel
      v-model="slide"
      height="1000px"
      control-color="primary"
      arrows
      infinite
      class="q-mt-xl"
    >
      <q-carousel-slide
        v-for="(image, index) in carouselImages"
        :key="index"
        :name="`slide${index + 1}`"
        :img-src="image"
      />
    </q-carousel>

    <!-- Produk -->
    <div class="q-mt-xl">
      <div class="text-h5 text-center q-mb-md">Produk Kami</div>
      <div class="row q-col-gutter-md justify-center">
        <q-card
          v-for="product in products"
          :key="product.id"
          class="my-card col-xs-12 col-sm-4"
        >
          <q-img
            :src="product.image"
            ratio="1"
            spinner-color="primary"
            :alt="product.name"
          />
          <q-card-section>
            <div class="text-h6">{{ product.name }}</div>
            <div class="text-subtitle2">Rp {{ product.price }}</div>
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

// Import gambar lokal
import produk1 from 'src/assets/images/produk1.jpg'
import produk2 from 'src/assets/images/produk2.jpg'
import produk3 from 'src/assets/images/produk3.jpg'

// Carousel pakai gambar lokal juga (opsional)
const carouselImages = [
  produk1,
  produk2,
  produk3,
]

const slide = ref('slide1')

const products = [
  { id: 1, name: 'Produk 1', price: '100.000', image: produk1 },
  { id: 2, name: 'Produk 2', price: '150.000', image: produk2 },
  { id: 3, name: 'Produk 3', price: '200.000', image: produk3 },
]
</script>

<style scoped>
.my-card {
  max-width: 300px;
}
</style>
