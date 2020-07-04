<template>
  <div class="todo-item" v-bind:class="{'is-complete': todos.completed}">
      <input type="checkbox" v-on:change="markComplete">
      <p>{{ todos.title }}</p>
  </div>
</template>

<script>
export default {
    name: "TodoItems",
    props: [ "todos" ],
    methods: {
        markComplete() {
            this.todos.completed = !this.todos.completed
        }
    }
}
</script>

<style scoped>
.todo-item{
    background: #f4f4f4;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
}

.is-complete{
    text-decoration: line-through;

}

.del{
    background: #ff0000;
    color: #fff;
    border:none;
    padding-inline: 5px 9px;
    cursor: pointer;
    float:right;
}
</style>