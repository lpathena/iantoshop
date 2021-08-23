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
      if(!this.title.trim()){
        return alert('输入不能为空');
      }
      const todoObj = {id:nanoid(), name: this.title, done: false}
      this.$emit('addAnItem',todoObj)
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
}
</script>

<style scoped>

</style>