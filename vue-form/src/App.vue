<template>
  <form v-on:submit="submitForm">
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
export default {
  data : function() {
    return {
      username:'',
      password:'',
    }
  },
  methods : {
    submitFrom: function(event) {
      event.preventDefault();
      console.log(this.username, this.password)
    }
  }
}
</script>

<style>

</style>