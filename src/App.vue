<template>
  <div>
    <Header></Header>
<!--    <router-link to="/">Home</router-link> |-->
<!--    <router-link to="/about">About</router-link>-->
  </div>
<!--  <router-view/>-->
</template>

<style>
@import 'assets/styles/generic/_base.css';
@import 'assets/styles/generic/_variable.css';
@import 'assets/styles/generic/_common.css';
@import 'boxicons';
</style>
<script>
import Header from "@/components/Header";
export default {
  components: {Header}
}
</script>