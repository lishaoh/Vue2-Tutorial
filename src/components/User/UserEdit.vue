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
export default {
  props: ["userAge"],
  methods: {
    editAge() {
      this.userAge = 28;
    }
  }
};
</script>
