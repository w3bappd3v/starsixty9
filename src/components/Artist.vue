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

<script>
  export default {
    methods: {
      handleClick() {
        this.$router.push({ name: 'artist', params: { id: this.id }});
      }
    }
  }
</script>

<template>
    <div @click="handleClick" class="artist">
      <h3 class="artist-name">{{ name }}</h3>
      <p class="description">{{ description }}</p>
      <slot></slot>
    </div>
</template> 

<style lang="scss" scoped>
    .artist {
        border: 1px solid #c8c8c8;
        border-radius: 6px;
        cursor: pointer;
        padding: 10px;
        margin-bottom: 20px;
        max-width: 480px;
    }
</style>