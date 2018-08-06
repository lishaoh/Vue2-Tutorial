<template>
<div class="component">
    <h1>The User Component</h1>
    <p>I am an awesome User !</p>
    <button @click="changeName">Change my Name</button>
    <hr>
    <div class="row">
        <div class="col-xs-12 col-sm-6">
            <user-detail :myName="name" @nameWasReset="name = $event" :resetFn="resetName" :userAge="userAge"></user-detail>
        </div>
        <div class="col-xs-12 col-sm-6">
            <user-edit :userAge="age"></user-edit>
        </div>
    </div>
</div>
</template>

<script>
import UserDetail from "./UserDetail.vue";
import UserEdit from "./UserEdit.vue";

export default {
  data: function() {
    return {
      name: "lsh",
      age: 24
    };
  },
  methods: {
    changeName: function() {
      this.name = "Andrew";
    },
    resetName() {
      this.name = "Andrew";
    },
    userAge() {
      this.age = 24;
    }
  },
  components: {
    UserDetail,
    UserEdit
  }
};
</script>

<style scoped>
div {
  background-color: lightblue;
}

.row {
  width: 100%;
  display: table;
}

.col-sm-6 {
  display: table-cell;
}
</style>
