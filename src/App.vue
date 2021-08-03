<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <MyHeader/>
    <Lists/>
    <MyFooter/>
  </div>
</template>

<script>

import Lists from './components/Lists'
import MyFooter from "./components/MyFooter";
import MyHeader from "./components/MyHeader";

export default {
  name: 'App',
  components: {
      MyHeader,MyFooter,Lists
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
