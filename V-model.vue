
<!-- html 부분 -->
<template>
    <div class="name">
      {{ name }}
    </div>
    <!-- <input type="text" :value="name" @input="updateName"> -->
    <!-- V-model : 양방향 binding 해주는 기능-->
    <input type="text" v-model="name">
    <button class="btn btn-primary" @click="updateName">Click</button>
  </template>
  
  <!-- js 부분 -->
  <script>
  import { ref } from "vue";
  
  export default {
    setup() {
      const name = ref('Happy');
  
      const onSubmit = () => {
        console.log(name.value)
      };
      
      // // 양방향 binding
      // const updateName = (e) => {
      //   console.log(e.target.value)
      //   name.value = e.target.value;
      // };
  
      return {
        name,
        onSubmit,
        // updateName,
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