
<!-- html 부분 -->
<template>
  <div :class="nameClass">
    {{ name }}
  </div>
  <!-- v-bind:value => :value -->
  <input :type="type" :value="name">
  <!-- v-on:click => @ -->
  <button class="btn btn-primary" v-on:click="updateName">Click</button>
</template>

<!-- js 부분 -->
<script>
import { ref } from "vue";

export default {
  setup() {
    const name = ref('Happy');
    const type = ref('number');
    const nameClass = ref('name');

    const updateName = () => {
      name.value = 'Corder'
      type.value = 'text'
    };

    return {
      name,
      updateName,
      type,
      nameClass,
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