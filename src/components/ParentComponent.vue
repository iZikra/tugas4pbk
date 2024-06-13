<template>
    <div class="parent">
      <h1>Parent Component</h1>
      <p>Message from Child: {{ message }}</p>
      <!-- Slot untuk menyisipkan konten dari child -->
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        message: ''
      };
    },
    methods: {
      receiveMessage(data) {
        this.message = data;
      }
    }
  };
  </script>
  
  <style scoped>
  .parent {
    padding: 20px;
    border: 2px solid #8B4513;
    border-radius: 10px;
    background-color: #FAEBD7;
    text-align: center;
  }
  h1 {
    color: #8B4513;
    font-family: 'Georgia', serif;
  }
  p {
    font-size: 18px;
    color: #555;
  }
  </style>
  