<template>
<div>
  <h2>New</h2>
  <button @click="counter++">Increase!</button>
  <p>{{counter}}</p>
</div>
</template>
<script>
export default {
  data: function() {
    return {
      counter: 0
    };
  },
  destroyed() {
    console.log("Destoryed!");
  },
  deactivated() {
    console.log("Deactivated!");
  },
  activated() {
    console.log("Activated!");
  }
};
</script>
<style scoped>
</style>
