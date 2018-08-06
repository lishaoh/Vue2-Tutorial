<template>
<div class="container">
    <appHeader></appHeader>
    <hr>
    <div class="row">
        <servers></servers>
        <server-details></server-details>
    </div>
    <hr>
    <app-footer></app-footer>
</div>
</template>

<script>
import Header from "./components/Shared/Header.vue";
import Footer from "./components/Shared/Footer.vue";
import Servers from "./components/Server/Servers.vue";
import ServerDetails from "./components/Server/ServerDetails.vue";

export default {
  components: {
    appHeader: Header,
    Servers,
    appFooter: Footer,
    ServerDetails
  }
};
</script>
