<template>
    <div class="parent">
      <h1>Parent Component</h1>
      <nested-child-component @send-data-to-parent="displayData"></nested-child-component>
      <slot></slot>
      <p class="received-data">{{ receivedData }}</p>
    </div>
  </template>
  
  <script>
  import NestedChildComponent from './NestedChildComponent.vue';
  
  export default {
    components: {
      NestedChildComponent
    },
    data() {
      return {
        receivedData: ''
      }
    },
    methods: {
      displayData(data) {
        this.receivedData = data;
      }
    }
  }
  </script>
  
  <style scoped>
  .parent {
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    width: 300px;
    text-align: center;
  }
  
  h1 {
    color: #333;
    font-size: 24px;
    margin-bottom: 20px;
  }
  
  .received-data {
    color: #FF5722;
    font-size: 16px;
    margin-top: 20px;
  }
  </style>
  