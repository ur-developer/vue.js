<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <lable for="username">id: </lable>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <lable for="password">password: </lable>
      <input id="password" type="password" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data : function() {
    return {
      username:'',
      password:'',
    }
  },
  methods : {
    submitFrom: function() {
      // event.preventDefault();
      console.log(this.username, this.password);
      var url = 'http://jsonplaceholder.typicode.com/users';
      var data = {
        username : this.username,
        password : this.password
      }         

      axios.post(url, data)
      .then(function(response) {
        console.log(response);
      })
      .catch(function(error) {
        console.log(error);
      });
    }
  }
}
</script>

<style>

</style>