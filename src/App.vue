<template>
  <div id="app">
    <parent-component>
      <template #default>
        <p class="slot-content">This is a slot content from parent.</p>
      </template>
    </parent-component>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  components: {
    ParentComponent
  }
}
</script>

<style>
#app {
  font-family: 'Arial', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: #f5f5f5;
}
 
.slot-content {
  color: #4CAF50;
  font-size: 18px;
  margin-top: 20px;
}
</style>
