<template>
  <div>
    <app-header></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

// var AppHeader = {
//   template 
// }
  // new Vue({
  //   data: {

  //   }
  // })

  export default {
  components: { AppHeader },
    data: function {
      return {
        str : 'hi'
      }
    }
    components {
      'app-header': AppHeader
    }
  }
</script>

<style>

</style>