<script setup>
    import Artist from '@/components/Artist.vue'
    import artists from '../data/artists.json'
</script>

<template>
    <Artist
        v-for="(artist, index) in artists"
        :name="artist.name"
        :description="artist.description"
    />
</template>