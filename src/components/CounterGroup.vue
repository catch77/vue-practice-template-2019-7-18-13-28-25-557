<template>
  <div id="CounterGroup">
  <Counter v-for="n in parseInt(counterNum)" 
    :key="n"
    @change="updateCount($event)" />
    <span>总数：{{total}}</span>
  </div>
</template>

<script>
import Counter from "./Counter";
export default {
  data: function() {
    return {
      total: 0
    }
  },
  components: {
    Counter
  },
  name: "CounterGroup",
  props: { counterNum: { default: 0 } },
  methods: {
    updateCount(num) {
      this.total = this.total + num;
    }
  }
};
</script>

<style>
</style>