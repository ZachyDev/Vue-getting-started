<template>
  <div class="hello">
    <h1> {{ msg }} </h1>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    }
  }
</script>

<!-- Adding "scoped" to limit the styling to this component only -->
<style scoped>

</style>



