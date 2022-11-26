<script setup>
    defineProps({
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
    <div class="artist">
        <h3 class="artist-name">{{ name }}</h3>
        <p class="description">{{ description }}</p>
    </div>
</template>

<style lang="scss" scoped>
    $base-color: rgb(219, 62, 62);
    .artist-name {
        color: $base-color;
    }
</style>