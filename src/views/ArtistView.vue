<script setup>
import Artist from '@/components/Artist.vue'
import Songs from '@/components/Songs.vue'
import artists from '../assets/data/artists.json'
</script>

<template>
    <h2>Artist Details</h2>
    <Artist :id="artist.id" :name="artist.name" :description="artist.description">
        <Songs :songs="artist.songs" />
    </Artist>
</template>

<script>
export default {
    components: {
        Artist,
        Songs,
    },
    data() {
        return {
            artist: {},
        }
    },
    created() {
        let routeId = this.$route.params.id;
        this.artist = artists.find(({ id }) => id === routeId);
    }
}
</script>

<style lang="scss" scoped>
    .artist {
        cursor: initial;
    }
</style>