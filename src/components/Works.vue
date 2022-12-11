<script>
  export default {
    props: {
      works: Array
    }
  }
</script>

<template>
  <div class="works">
    <h4>Works</h4>
    <ul>
      <li v-for="(work, index) in works">
        {{ work.name }}
      </li>
    </ul>
  </div>
</template> 

<style lang="scss" scoped>
  .works {
    padding: 10px;
  }
</style>