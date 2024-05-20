<script setup>
import { onMounted, ref } from 'vue'
import PostService from '@/services/PostService.js'
import BlogCard from '@/components/BlogCard.vue'

const posts = ref(null)

onMounted(() => {
 PostService.getPosts()
    .then((response) => {
      posts.value = response.data
      console.log(posts.value[0])
    })
    .catch((error) => {
      console.log(error)
    })
})
</script>

<template>
<h1>Blog</h1>
  <BlogCard class="post" v-for="post in posts" key="post.id" :post="post" />
</template>

<style scoped>
.posts {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>