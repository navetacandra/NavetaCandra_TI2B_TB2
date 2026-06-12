<script setup lang="ts">
import { RouterView } from 'vue-router'
import AppNavbar from './components/AppNavbar.vue'
</script>

<template>
  <div class="app-container">
    <AppNavbar />
    <RouterView />
  </div>
  <footer class="footer">
    <p>Copyright 2026 &copy; Aricand's Cake</p>
  </footer>
</template>

<style>
.app-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>
