<script>
  export default {
    props: {
      works: Array
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
    <ul>
      <li v-for="(work, index) in works">
        {{ work.title }}
        <ul>
          <li v-for="(piece, index) in work.pieces">
            {{ piece.name }}
            <audio controls>
              <source :src="piece.path" type="audio/mpeg">
              Your browser does not support the audio element.
            </audio>      
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template> 

<style lang="scss" scoped>
  .works {
    padding: 10px;
  }
</style>