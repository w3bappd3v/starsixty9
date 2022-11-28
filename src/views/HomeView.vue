<script setup>
import artists from '../assets/data/artists.json'
import Artist from '@/components/Artist.vue'
</script>

<template>
  <main>
    <h2>Featured Artist</h2>
    <Artist
        :id="artists[0].id"
        :name="artists[0].name"
        :description="artists[0].description"
    />
  </main>
</template>
