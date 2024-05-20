<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div id="layout">
    <header>
      <div class="wrapper">
        <nav>
          <RouterLink :to="{ name: 'event-list'}">Events</RouterLink>
          <RouterLink :to="{ name: 'about'}">About</RouterLink>
          <RouterLink :to="{ name: 'posts-list'}">Blog</RouterLink>
        </nav>
      </div>
    </header>
    <RouterView />
  </div>
</template>

<style>
  #layout {
    font-family: Avenir, Helvetica, sans-serif;
    text-align: center;
    color: #2c3e50;
  }
  nav {
    padding: 30px;
  }
  nav a {
    font-weight: bold;
    color: #2c3e50;
    margin-right: 10px;
  }
  nav a.router-link-exact-active {
    color: #42b983;
  }
  h2 {
    font-size: 20px;
  }
</style>
