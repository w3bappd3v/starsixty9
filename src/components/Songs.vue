<script>
  export default {
    props: {
      songs: Array
    }
  }
</script>

<template>
  <div class="songs">
    <h4>Songs</h4>
    <ul>
      <li v-for="(song, index) in songs">
        {{ song }}
      </li>
    </ul>
  </div>
</template> 

<style lang="scss" scoped>
  .songs {
    padding: 10px;
  }
</style>