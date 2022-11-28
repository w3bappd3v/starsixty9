<script setup>
    import Artist from '@/components/Artist.vue'
    import artists from '../assets/data/artists.json'
</script>

<template>
    <h2>Artist Details</h2>
    <Artist
        :id="artist.id"
        :name="artist.name"
        :description="artist.description"
    />
</template>

<script>
    export default {
        data(){
            return {
                artist: {},
            }
        },
        created(){
            let routeId=this.$route.params.id;
            this.artist = artists.find(({ id }) => id === routeId);            
        }
    }
</script>