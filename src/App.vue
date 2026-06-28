<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>
  </header>
  <main>
    <RouterView />
  </main>
</template>

<style scoped>
header {
  background: #1a73e8;
  padding: 0 2rem;
}

nav {
  display: flex;
  gap: 1.5rem;
  padding: 1rem 0;
}

nav a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  transition: background 0.2s;
}

nav a:hover,
nav a.router-link-active {
  background: rgba(255, 255, 255, 0.2);
}
</style>
