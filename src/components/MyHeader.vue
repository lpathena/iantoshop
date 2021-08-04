<template>
  <div>
    <input type="text" @keyup.enter="add"/>
  </div>
</template>

<script>

import { nanoid } from 'nanoid'

export default {
  name: "MyHeader",
  methods:{
    add(e){
      const todoObj = {id:nanoid(), name: e.target.value, done: false}
      this.addAnItem(todoObj)
      e.target.value = ''
    }
  },
  props:['addAnItem'],
}
</script>

<style scoped>

</style>