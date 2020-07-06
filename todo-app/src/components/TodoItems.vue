<template>
  <div class="todo-items" v-bind:class="{'is-complete':todos.completed}">
      <p>
          <input type="checkbox" v-on:change="markCompleted">
      {{ todos.title }}
      <button @click="$emit('del-todo',todos.id)" class="del">x</button>
      </p>
  </div>
</template>

<script>
export default {
    name: "TodoItems",
    props: [ "todos" ],
    methods: {
        markCompleted(){
            this.todos.completed = !this.todos.completed;
        }
    }
}
</script>

<style>
.todo-items{
    background-color: #f4f4f4;
    padding: 10px;
    border-bottom: 1px solid #ccc;
}
.is-complete{
    text-decoration: line-through;
}
.del{
    background-color:#ff0000;
    padding: 5px 10px;
    color:#fff;
    border-radius: 40px;
    float:right;
    outline: none;
    border: 1px solid #ccc;
    cursor:pointer;
}
</style>