<script setup>
    defineProps({
      id: {
        type: String,
        required: true
      },
      name: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
    })
</script>

<template>
    <RouterLink class="artist" :to="{ name: 'artist', params: { id: id }}">
        <h3 class="artist-name">{{ name }}</h3>
        <p class="description">{{ description }}</p>
    </RouterLink></template> 

<style lang="scss" scoped>
    $base-color: rgb(219, 62, 62);
    .artist-name {
        color: $base-color;
    }
</style>