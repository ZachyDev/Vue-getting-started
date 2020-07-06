<template>
  <div class="todo-item" v-bind:class="{'is-complete': todos.completed}">
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
        markCompleted() {
            this.todos.completed = !this.todos.completed;
        }
    }
}
</script>

<style>
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
    padding: 5px 10px;
    cursor: pointer;
    float:right;
    border-radius: 40px;
}
</style>