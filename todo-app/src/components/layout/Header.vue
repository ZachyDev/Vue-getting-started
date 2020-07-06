<template>
  <header class="header">
      <h1>TodoList</h1>
      <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      </div>
  </header>
</template>

<script>
export default {
    name: "header"
}
</script>

<style scoped>
    .header{
        background: #333;
        color:#fff;
        padding:10px;
        text-align: center;
    }
    .header a {
        color: #fff;
        padding-right: 5px;
        text-decoration: none;
    }
</style>