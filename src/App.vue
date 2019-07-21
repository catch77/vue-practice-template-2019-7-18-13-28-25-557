<template>
  <div id="app">
      <span>请输入数字：</span>
      <input v-model="number">
    <CounterGroup v-bind:counterNum="number" @change="(val) => updateCount(index, val)"></CounterGroup>
    
  </div>
</template>

<script>
import CounterGroup from "./components/CounterGroup"
export default {
  name: 'app',
  components: {
    CounterGroup
  },
  data: function() {
    return {
      number: 0
    }
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
