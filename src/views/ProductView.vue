<script setup lang="ts">
import AppProductCard from '../components/AppProductCard.vue'

const products = [
  { name: 'Onde-Onde', img: '6149853402612044416.jpg' },
  { name: 'Pie Buah', img: '6149853402612044417.jpg' },
  { name: 'Bolu Kukus', img: '6149853402612044418.jpg' },
  { name: 'Bolu Gula Merah Kukus', img: '6149853402612044419.jpg' },
  { name: 'Martabak Mini', img: '6149853402612044420.jpg' },
  { name: 'Sosis Solo', img: '6149853402612044421.jpg' },
  { name: 'Bakpao Coklat', img: '6149853402612044422.jpg' },
  { name: 'Nona Manis', img: '6149853402612044423.jpg' },
  { name: 'Pastel Sayur', img: '6149853402612044424.jpg' },
  { name: 'Nagasari', img: '6149853402612044425.jpg' },
  { name: 'Bugis', img: '6149853402612044426.jpg' },
]
</script>

<template>
  <div class="product-page">
    <main>
      <section class="products-all">
        <h1>Produk Kami</h1>
        <div class="product-grid">
          <AppProductCard v-for="p in products" :key="p.img" :name="p.name" :image="p.img" />
        </div>
      </section>
    </main>
  </div>
</template>
