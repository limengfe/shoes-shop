<template>
  <div id="app">
    <keep-alive> <router-view></router-view></keep-alive>
    <main-tar-bar></main-tar-bar>
  </div>
</template>

<script>
import MainTarBar from "components/contents/maintarbar/MainTarBar";
export default {
  name: "app",
  components: {
    MainTarBar,
  },
};
</script>

<style>
/*css 引入方式*/
@import "assets/css/base.css";
</style>
