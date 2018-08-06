<template>
<div class="container">
    <appHeader></appHeader>
    <hr>
    <div class="row">
        <servers></servers>
        <server-details></server-details>
    </div>
    <hr>
    <user></user>
    <app-footer></app-footer>
</div>
</template>

<script>
import Header from "./components/Shared/Header.vue";
import Footer from "./components/Shared/Footer.vue";
import Servers from "./components/Server/Servers.vue";
import ServerDetails from "./components/Server/ServerDetails.vue";
import User from "./components/User/User";

export default {
  components: {
    appHeader: Header,
    Servers,
    appFooter: Footer,
    ServerDetails,
    User
  }
};
</script>

<style>
div.component {
  border: 1px solid black;
  padding: 30px;
}
</style>
