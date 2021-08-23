<template>
  <div>
    <input type="text" v-model="title" @keyup.enter="add"/>
    <button @click="testWindows">点我一下试试</button>
    <button @click="unbindCustomEvent">click me</button>
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
    },
    testWindows(){
      this.$emit('languh','name','agender','abc')
    },
    unbindCustomEvent(){
      this.$off('languh')
      // this.$off(['languh','event2'])
      // this.$off()
    }
  },
  props:['addAnItem'],
}
</script>

<style scoped>

</style>