<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="center-me">
    <header>
      <h1>Starsixty9</h1>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/artists">Artists</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </header>
  
    <RouterView />
  </div>
</template>

<style lang="scss" scoped>
.center-me {
  max-width: 500px;
  margin: auto;
  header {
    display: flex;
    align-items: center;
  }
  
  nav {
    font-size: 12px;
    text-align: center;
    a {
      color: #2786ce;
      font-size: 1.5em;
      text-decoration: none;
  
      &:hover {
        color: #cb6161;
      }
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
}


</style>
