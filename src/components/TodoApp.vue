<script setup>
import TodoForm from "./TodoForm.vue";
import TodoList from "./TodoList.vue";
import { useTodoListStore } from "@/stores/TodoListStore";

const store = useTodoListStore();

const { clearList } = store;
</script>

<template>
  <div class="todo-app">
    <h1>To Do List</h1>
    <todo-form />
    <todo-list />
    <button @click="clearList()">Clear the List</button>
  </div>
</template>

<style scoped>
.todo-app {
  padding: 5vh;
  min-height: 100vh;
  width: 30vw;
  background-color: #f7f9fc;
}
button {
  margin-left: 30px;
  background-color: #2f6089;
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  font-weight: 800;
  color: white;
  width: 40%;
}
</style>
