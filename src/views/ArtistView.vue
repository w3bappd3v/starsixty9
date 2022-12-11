<script setup>
import Artist from '@/components/Artist.vue'
import Works from '@/components/Works.vue'
import artists from '../assets/data/artists.json'
</script>

<template>
    <h2>Artist Details</h2>
    <Artist :id="artist.id" :name="artist.name" :description="artist.description">
        <Works :works="artist.works" />
    </Artist>
</template>

<script>
export default {
    components: {
        Artist,
        Works,
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