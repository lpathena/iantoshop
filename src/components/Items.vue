<template>
  <li>
    <label>
      <input type="checkbox" :checked="todo.done" @change="handleCheck(todo.id)"/>
      <span>{{ todo.name }}</span>
    </label>
  </li>
</template>

<script>
export default {
  name: "Items",
  props:['todo','changeStatus'],
  methods:{
    handleCheck(id){
      // console.log('@',id)
      this.changeStatus(id)
    }
  },
}
</script>

<style scoped>

</style>