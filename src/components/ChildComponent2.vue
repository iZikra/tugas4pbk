<template>
    <div class="child">
      <h2>Child Component 2</h2>
      <button @click="sendMessage">Send Message</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendMessage() {
        this.$emit('send-message', 'Message from Child Component 2');
      }
    }
  };
  </script>
  
  <style scoped>
  .child {
    padding: 10px;
    margin: 10px;
    border: 2px solid #8A2BE2;
    border-radius: 10px;
    background-color: #F5F5DC;
    text-align: center;
  }
  h2 {
    color: #8A2BE2;
    font-family: 'Georgia', serif;
  }
  button {
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    background-color: #8A2BE2;
    color: white;
    font-size: 16px;
    cursor: pointer;
    font-family: 'Georgia', serif;
  }
  button:hover {
    background-color: #A64BE5;
  }
  </style>
  