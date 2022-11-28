<script setup>
    import Artist from '@/components/Artist.vue'
    import artists from '../assets/data/artists.json'
</script>

<template>
    <h2>All Artists</h2>
    <Artist
        v-for="(artist, index) in artists"
        :id="artist.id"
        :name="artist.name"
        :description="artist.description"
    />
</template>