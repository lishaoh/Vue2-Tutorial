<template>
<div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
        <div class="panel-body quote">
          <slot></slot>
        </div>
    </div>
</div>
</template>

<script>
// export default {
//   props: ["quote"]
// };
</script>

<style scoped>
.panel-body {
  font-family: "Arizonia", cursive;
  font-size: 24px;
  color: #6e6e66;
}

.quote {
  cursor: pointer;
}

.quote:active {
  background-color: #ffe2f2;
}
</style>
