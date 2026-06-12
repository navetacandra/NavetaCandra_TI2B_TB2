<script setup lang="ts">
defineProps<{
  name: string
  image: string
}>()

const getImageUrl = (name: string) => {
  return new URL(`../produk/${name}`, import.meta.url).href
}
</script>

<template>
  <div class="product-card" :style="{ backgroundImage: `url(${getImageUrl(image)})` }">
    <div class="product-overlay">
      <span class="product-name">{{ name }}</span>
    </div>
  </div>
</template>
