<template>
    <div class="child">
      <h2>Child Component 1</h2>
      <button @click="sendMessage">Send Message</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendMessage() {
        this.$emit('send-message', 'Message from Child Component 1');
      }
    }
  };
  </script>
  
  <style scoped>
  .child {
    padding: 10px;
    margin: 10px;
    border: 2px solid #4682B4;
    border-radius: 10px;
    background-color: #E6E6FA;
    text-align: center;
  }
  h2 {
    color: #4682B4;
    font-family: 'Georgia', serif;
  }
  button {
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    background-color: #4682B4;
    color: white;
    font-size: 16px;
    cursor: pointer;
    font-family: 'Georgia', serif;
  }
  button:hover {
    background-color: #5A9BD3;
  }
  </style>
  