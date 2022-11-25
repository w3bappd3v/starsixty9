<script setup>
import artists from '../data/artists.json'
import Artist from '@/components/Artist.vue'
</script>

<template>
  <main>
    <Artist
        :name="artists[0].name"
        :description="artists[0].description"
    />
  </main>
</template>
