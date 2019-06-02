<template>
  <div class="wrapper">
    <MyHeader/>
    <MyMain/>
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from "./components/Header";
import MyMain from "./components/Main";
import MyFooter from "./components/Footer";
export default {
  components: {
    MyHeader,
    MyMain,
    MyFooter
  }
};
</script>

<style>
</style>
