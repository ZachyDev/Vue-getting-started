<template>
  <div>
      <div v-bind:key = "todo.id" v-for="todo in todos">
        <TodoItems v-bind:todos="todo" v-on:del-todo="$emit('del-todo',todo.id)"/>
        
      </div>
  </div>
</template>

<script>
// import TodoItems component
import TodoItems from './TodoItems';
export default {
    name: "Todos",
    components: {
      TodoItems
    },
    props: [ "todos" ]
}
</script>

<style scoped>

</style>