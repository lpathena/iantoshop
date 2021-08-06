<template>
  <ul>
    <Items v-for="todoObj in todos" :key="todoObj.id" :todo="todoObj" :changeStatus="changeStatus" :deleteTodoObj="deleteTodoObj"/>
  </ul>
</template>

<script>
import Items from "./Items";


export default {
  name: "Lists",
  components: {Items},
  props:['todos','changeStatus','deleteTodoObj'],
}
</script>

<style scoped>

</style>