<template>
    <div class="child">
      <p>Child Component</p>
      <button @click="sendDataToParent" class="btn">Click me to send data to parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendDataToParent() {
        this.$emit('send-data', 'Data from Child Component');
      }
    }
  }
  </script>
  
  <style scoped>
  .child {
    background: #ffecb3;
    padding: 10px;
    border-radius: 5px;
  }
  
  .btn {
    background: #4CAF50;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s;
  }
  
  .btn:hover {
    background: #45a049;
  }
  </style>
  