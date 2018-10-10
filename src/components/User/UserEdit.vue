<template>
  <div>
    <h3>You may edit the User here</h3>
    <p>Edit me !</p>
    <p>User Age: {{userAge}}</p>
    <button @click="editAge">Edit Age</button>
  </div>
</template>

<style scoped>
div {
  background-color: lightcoral;
  padding: 30px;
}
</style>

<script>
import { eventBus } from "../../main.js";
export default {
  props: ["userAge"],
  methods: {
    editAge() {
      eventBus.changeAge(28);
      // this.userAge = 28;
      // eventBus.$emit("ageWasEdit", 28);
    }
  }
};
</script>
