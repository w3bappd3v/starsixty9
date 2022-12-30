<script>
  export default {
    props: {
      works: Object
    },
    methods: {
      getWorks() {
        return this.works.pieces;
      }
    }
  }
</script>

<template>
  <div class="works">
    <h4>Works</h4>
    <p>{{ works.type }}</p>
    <ul>
      <li v-for="(piece, index) in works.pieces">
        {{ piece.name }}
        <audio controls>
          <source :src="piece.path" type="audio/mpeg">
          Your browser does not support the audio element.
        </audio>
      </li>
    </ul>
  </div>
</template> 

<style lang="scss" scoped>
  .works {
    padding: 10px;
  }
</style>