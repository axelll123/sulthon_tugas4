<template>
    <div class="nested-child">
      <p>Nested Child Component</p>
      <child-component @send-data="receiveDataFromChild"></child-component>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    components: {
      ChildComponent
    },
    methods: {
      receiveDataFromChild(data) {
        this.$emit('send-data-to-parent', data);
      }
    }
  }
  </script>
  
  <style scoped>
  .nested-child {
    background: #e0f7fa;
    padding: 10px;
    border-radius: 5px;
    margin-bottom: 20px;
  }
  </style>
  