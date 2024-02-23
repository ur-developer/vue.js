
<!-- html 부분 -->
<template>
    <div class="name">
      {{ name }}
    </div>
    <button class="btn btn-primary" v-on:click="updateName">Click</button>
  </template>
  
  <!-- js 부분 -->
  <script>
  // import { reactive } from "vue"; // reactive array와 object만 가능하다. 
   import { ref } from "vue"; // ref 모든 값 가능 단, value라는 값과 사용해야한다.
  
  export default {
    // setup()
    // setup vue3에서만 사용가능. component 내부에서만 사용가능
    // component의 data , method 등을 정의하고 반환흔 역할을 함
    // 함수는 component가 생성될 때 호출, component 초기화 작업을 수행
    // Vue3의 Composition API에서 사용되는 함수
    
    // const : 상수를 선언할때 사용 , 한번 할당된 값을 변경할 수 없음
    // 블록범위로 제한, 변수가 선언되고 초기화되지 않으면 오류 발생
    // Ex) Const number = 3.14; Number = 3; => 에러 발생
  
    // let : 변수를 선언할때 사용, 
    // 변수의 값을 변경 할 수 있음 , 블로 범위로 제한
    // 변수가 선언되고 초기화 하지 않으면 undefined로 설정됨
    // Ex) Let count = 0; Count = 1; => 가능
  
    // Var : 재사용 가능
    
    setup() {
      // let name = ref('Happy Corder1');
      // const name = reactive({
      //   id : 1
      // })
      
      const name = ref({
        id : 1
      });
      
      const updateName = () => {
        // name = 'Happy Corder';
        // name.value = 'Happy Corder';
        // name.id = 2;
        name.value.id = 2;
      }
  
      return {
        name,
        updateName,
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