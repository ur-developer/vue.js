
<!-- html 부분 -->

<template>
    <div class="container">
      <h2>To-do List</h2>
      <form @submit.prevent="onSubmit" class="d-flex">
        <div class="flex-grow-1 mr-2">
          <input class="form-control" type="text" v-model="todo" placeholder="type new to-do">
        </div>
        <div>
          <button class="btn btn-primary" type="submit">Add</button>
        </div>
      </form>
      {{ todos }}
    </div>
  </template>
  
  <!-- js 부분 -->
  <script>
  import { ref } from "vue";
  
  export default {
    setup() {
      const todo = ref('');
      const todos = ref([]);
  
      const onSubmit = () => {
        // e.preventDefault();
        todos.value.push({
          id: Date.now(),
          subject: todo.value,
        });
      };
  
      return {
        todo,
        todos,
        onSubmit,
  
      };
    },
  };
  </script>
  
  <!-- css 부분 -->
  <style>
  .name {
    color: red;
  }
  </style>