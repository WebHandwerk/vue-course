<script setup>
 defineProps({
   posts: {
     type: Object,
     required: true
   }
 })
</script>

<template>
  <div class="blog-card">
    <h2>{{ posts.title }}</h2>
  </div>
</template>

<style scoped>

</style>