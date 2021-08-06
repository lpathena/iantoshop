<template>
  <ul>
    <Items v-for="todoObj in todos" :key="todoObj.id" :todo="todoObj" :changeStatus="changeStatus"/>
  </ul>
</template>

<script>
import Items from "./Items";


export default {
  name: "Lists",
  components: {Items},
  props:['todos','changeStatus'],
}
</script>

<style scoped>

</style>