<template>
<div>
    <h3>You may view the User Details here</h3>
    <p>Many Details</p>
    <p>User Name: {{ switchName()}}</p>
    <p>User Age: {{ userAge}}</p>
    <button @click="resetName">ResetName</button>
    <button @click="resetFn">ResetName</button>
</div>
</template>

<script>
import { eventBus } from "../../main.js";

export default {
  props: {
    myName: {
      type: String
    },
    resetFn: Function,
    userAge: Number
  },
  methods: {
    switchName() {
      return this.myName
        .split("")
        .reverse()
        .join("");
    },
    resetName() {
      this.$emit("nameWasReset", "lsh");
    }
  },
  created() {
    // eventBus.$on("ageWasEdit", age => {
    //   this.userAge = age;
    // });
  }
};
</script>

<style scoped>
div {
  background-color: orange;
  padding: 30px;
}
</style>
