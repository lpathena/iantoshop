<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <MyHeader :addAnItem="addAnItem"/>
    <Lists :todos="todos"/>
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
  },
  data(){
    return {
      todos:[
        {id:'001',name:'eating',done:false}
      ]
    }
  },
  methods:{
    addAnItem(todoObj){
      this.todos.unshift(todoObj)
    }
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
