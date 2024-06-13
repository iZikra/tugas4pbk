<template>
    <div class="child">
      <h2>Child Component 3</h2>
      <button @click="sendMessage">Send Message</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendMessage() {
        this.$emit('send-message', 'Message from Child Component 3');
      }
    }
  };
  </script>
  
  <style scoped>
  .child {
    padding: 10px;
    margin: 10px;
    border: 2px solid #228B22;
    border-radius: 10px;
    background-color: #FFF8DC;
    text-align: center;
  }
  h2 {
    color: #228B22;
    font-family: 'Georgia', serif;
  }
  button {
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    background-color: #228B22;
    color: white;
    font-size: 16px;
    cursor: pointer;
    font-family: 'Georgia', serif;
  }
  button:hover {
    background-color: #32CD32;
  }
  </style>
  