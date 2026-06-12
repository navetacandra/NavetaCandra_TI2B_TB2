<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <nav class="navbar">
    <div class="logo">Aricand's Cake</div>
    <ul class="nav-links">
      <li><RouterLink to="/" active-class="active">Home</RouterLink></li>
      <li><RouterLink to="/about" active-class="active">About</RouterLink></li>
      <li><a href="#">Produk</a></li>
    </ul>
  </nav>
</template>
