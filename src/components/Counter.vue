<template>
  <div id="Counter">
    <span>{{count}}</span>
    <button @click="add">点我+</button>
    <button @click="decrease">点我-</button>
  </div>
</template>

<script>

export default {
  name: 'Counter',
  data: function() {
    return {
      count: 0
    }
  },
  methods:{
    add: function() {
      this.count++,
      this.$emit('change', 1)
    },
    decrease: function() {
      this.count--
      this.$emit('change', -1)
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