<template>
  <div id="app">
    <h1 class="mx-auto text-primary" style="padding-bottom: 50px;"><b>Todo</b></h1>
      <Todos v-bind:todos="todos"/>
  </div>
</template>

<script>
import Todos from "./components/Todos";

export default {
  name: 'App',
  components: {
    Todos
  },

  data() {
    return {
      todos: null
    }
  },
   async created(){
      const res = await fetch('https://jsonplaceholder.typicode.com/todos/');
      const data = await res.json();
      console.log(data)
      this.todos = data;
  },
}
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
</style>
