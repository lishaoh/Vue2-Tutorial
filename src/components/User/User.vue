<template>
<div class="component">
    <h1>The User Component</h1>
    <p>I am an awesome User !</p>
    <button @click="changeName">Change my Name</button>
    <p>Name is {{name}}</p>
    <p>Age is {{age}}</p>
    <hr>
    <div class="row">
        <div class="col-xs-12 col-sm-6">
            <user-detail :myName="name" @nameWasReset="name = $event" :resetFn="resetName" :userAge="age"></user-detail>
        </div>
        <div class="col-xs-12 col-sm-6">
            <user-edit :userAge="age" @ageWasEdit="age = $event"></user-edit>
        </div>
    </div>
</div>
</template>

<script>
import UserDetail from "./UserDetail.vue";
import UserEdit from "./UserEdit.vue";
import { eventBus } from "../../main.js";

export default {
  data: function() {
    return {
      name: "lsh",
      age: 25
    };
  },
  methods: {
    changeName: function() {
      this.name = "Andrew101";
    },
    resetName() {
      this.name = "Andrew";
    },
    userAge() {
      this.age = 24;
    }
  },
  created() {
    eventBus.$on("ageWasEdit", age => {
      this.age = age;
    });
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
