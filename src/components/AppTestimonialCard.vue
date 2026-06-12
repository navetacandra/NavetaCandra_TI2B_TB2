<script setup lang="ts">
defineProps<{
  name: string
  comment: string
}>()
</script>

<template>
  <div class="testimoni-card">
    <p class="comment">"{{ comment }}"</p>
    <p class="name">- {{ name }}</p>
  </div>
</template>
