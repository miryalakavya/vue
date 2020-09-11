<template>
  <div id="app">
    <input type="text" id="input" v-model="msg" placeholder="Enter something"/> <br><br><br>
    <button id="click" type="button" @click="click">Submit</button><br><br>
    <p id="input"> {{msg | toUpper }}</p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
   return {
     msg: ''
   }
  },
  methods: {
    click() {
      this.msg = this.msg.toUpperCase();
    }
  }
}
  
</script>

<style>
  #app {
    margin-left: 36%;
    margin-top: 10%;
  }
  #click {
    margin-left: 16%;
    cursor: pointer;
    background-color: black;
    color: white;
    width: 80px;
    height: 25px;
    border: 2px dotted red;
    border-radius: 10px;
  }
  #input {
    border: 2.5px solid skyblue;
    border-radius: 20px;
    width: 350px;
    height: 30px;
  }
  #input:hover {
    border: 2.5px solid red;
  }
</style>
