<!-- html 부분 -->
<template>
    <!-- <div class="name">
      {{ greeting(name) }}
    </div>
     -->
    <div class="name">
      {{ greet }}
    </div>
  </template>
  
  <!-- js 부분 -->
  <script>
  export default {
    setup() {
      const name = "Happy Corder";
      const greeting = (name) => {
        return "Hello, " + name;
      };
  
      const greet = greeting(name);
  
      return {
        // name,
        // greeting,
        greet,
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