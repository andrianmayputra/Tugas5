<template>
  <q-layout view="lHh lpr lFf">
    <landing-page></landing-page>
  </q-layout>
</template>

<script>
import LandingPage from './components/LandingPage.vue';

export default {
  name: 'App',
  components: {
    LandingPage,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  margin: 0;
  padding: 0;
  font-family: 'Open Sans', sans-serif;
  background-color: #f5f5f5;
}
</style>

<!--<template>
  <div class="q-pa-md q-gutter-sm">
    <q-btn color="white" text-color="black" label="Standard" />
    <q-btn color="primary" label="Primary" />
    <q-btn color="secondary" label="Secondary" />
    <q-btn color="amber" glossy label="Amber" />
    <q-btn color="brown-5" label="Brown 5" />
    <q-btn color="deep-orange" glossy label="Deep Orange" />
    <q-btn color="purple" label="Purple" />
    <q-btn color="black" label="Black" />
  </div>
</template>-->

<!-- <template>
  <div class="todo-app">
    <form @submit.prevent="addTodo" class="todo-form">
      <input v-model="newTodo" required placeholder="Masukkan TODO" class="todo-input">
      <button type="submit" class="todo-button">Add Todo</button>
    </form>
    <ul class="todo-list">
      <li v-for="todo in filteredTodos" :key="todo.id" class="todo-item">
        <input type="checkbox" v-model="todo.done">
        <span class="{ done: todo.done }">{{ todo.text }}</span>
        <button @click="removeTodo(todo)" class="delete-button">X</button>
      </li>
    </ul>
    <button @click="hideCompleted = !hideCompleted" class="toggle-completed">
      {{ hideCompleted ? 'Show all': 'Hide completed' }}
    </button>
  </div>
</template> -->
<!-- 
<script setup>
  import { ref, computed, onUpdated } from 'vue'

  onUpdated(() => {
    console.log("berubah oi")
  })

  let id = 0
  const newTodo = ref('')
  const hideCompleted = ref(false) 

  const todos = ref([
    { id: id++, text: 'Learn HTML', done: true },
    { id: id++, text: 'Learn CSS', done: false },
    { id: id++, text: 'Learn JavaScript', done: true },
    { id: id++, text: 'Learn Vue', done: false },
  ])

  const filteredTodos = computed(() => {
    return hideCompleted.value ? todos.value.filter((t) => !t.done) : todos.value
  })

  function addTodo() {
    todos.value.push({ id: id++, text: newTodo.value, done: false })
    newTodo.value = ''
  }

  function removeTodo(todo) {
    const index = todos.value.indexOf(todo)
    if (index !== -1) {
      todos.value.splice(index, 1)
    }
  }
</script>

<style>
  .todo-input {
    margin: 0 20px 5px 1px;
    padding: 5px;
  }

  .todo-button {
    color: white;
    background-color: green;
    padding: 4px;
    border-radius: 4x;
    cursor: pointer;
  }

  .delete-button {
    margin-left: 13px;
    color: white;
    background-color: red;
    cursor: pointer;
  }

  .done {
    text-decoration: line-through;
  }
</style> -->
