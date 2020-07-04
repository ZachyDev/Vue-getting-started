<template>
  <div id="app">
    <HelloWorld msg = "CodeWithZachy"/>
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld';
  export default {
    name: 'App',
    components: {
      HelloWorld
    }
  }
</script>

<style>
#app{
  color:#42b983;
  position: relative;
  margin-top:60px;

}
</style>