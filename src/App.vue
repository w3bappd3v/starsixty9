<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <h1>Starsixty9</h1>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/artists">Artists</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style lang="scss" scoped>
header {
  display: flex;
  align-items: center;
}

nav {
  font-size: 12px;
  text-align: center;
  a {
    color: rgb(39, 134, 206);
  }
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

</style>
