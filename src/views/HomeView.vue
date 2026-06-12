<script setup lang="ts">
import AppTestimonialCard from '../components/AppTestimonialCard.vue'
import AppProductCard from '../components/AppProductCard.vue'

const products = [
  { name: 'Onde-Onde', img: '6149853402612044416.jpg' },
  { name: 'Pie Buah', img: '6149853402612044417.jpg' },
  { name: 'Bolu Kukus', img: '6149853402612044418.jpg' },
  { name: 'Bolu Gula Marah Kukus', img: '6149853402612044419.jpg' },
  { name: 'Martabak Mini', img: '6149853402612044420.jpg' },
  { name: 'Sosis Solo', img: '6149853402612044421.jpg' },
]

const heroImages = ['6149853402612044422.jpg', '6149853402612044423.jpg', '6149853402612044424.jpg']

const testimonials = [
  { name: 'Bu Ali', comment: 'Sosis solo-nya enak banget. Andalan cemilan untuk acara-acara.' },
  {
    name: 'Bu Roni',
    comment: 'Pastel-nya juara. Enak dan sesuai harga-nya, nikmat buat cemilan bareng keluarga.',
  },
  {
    name: 'Bu Imam',
    comment: 'Kue jajanan pasarnya enak dan ramah di kantong. Pas banget untuk snack acara-acara.',
  },
]

const getImageUrl = (name: string) => {
  return new URL(`../produk/${name}`, import.meta.url).href
}
</script>

<template>
  <div class="home-page">
    <main>
      <section class="hero">
        <div class="tagline">
          <h1>Lezatnya Tradisi,<br />Sehatnya Nutrisi</h1>
          <p>Nikmati ragam jajanan pasar pilihan yang dibuat dari bahan alami tanpa pengawet.</p>
        </div>
        <div class="hero-images">
          <div
            v-for="(img, index) in heroImages"
            :key="img"
            :class="['stacked-card', `card-${index + 1}`]"
            :style="{ backgroundImage: `url(${getImageUrl(img)})` }"
          ></div>
        </div>
      </section>

      <section class="testimonials">
        <AppTestimonialCard
          v-for="t in testimonials"
          :key="t.name"
          :name="t.name"
          :comment="t.comment"
        />
      </section>

      <section class="products">
        <h2>Produk Unggulan</h2>
        <div class="product-grid">
          <AppProductCard v-for="p in products" :key="p.img" :name="p.name" :image="p.img" />
        </div>
        <a href="#" class="show-more">Lihat Semua Produk</a>
      </section>
    </main>
  </div>
</template>
