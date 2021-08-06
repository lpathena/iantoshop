<template>
  <div>
    <input type="text" v-model="title" @keyup.enter="add"/>
  </div>
</template>

<script>

import { nanoid } from 'nanoid'

export default {
  name: "MyHeader",
  data(){
    return {
      title:''
    }
  },
  methods:{
    add(){
      // add(e){
      if(!this.title.trim()){
        return alert('输入不能为空');
      }
      const todoObj = {id:nanoid(), name: this.title, done: false}
      // const todoObj = {id:nanoid(), name: e.target.value, done: false}
      this.addAnItem(todoObj)
      // e.target.value = ''
      this.title = ''
    }
  },
  props:['addAnItem'],
}
</script>

<style scoped>

</style>