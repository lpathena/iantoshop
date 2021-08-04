<template>
  <ul>
    <Items v-for="todoObj in todos" :key="todoObj.id" :todo="todoObj"/>
  </ul>
</template>

<script>
import Items from "./Items";


export default {
  name: "Lists",
  components: {Items},
  props:['todos'],
}
</script>

<style scoped>

</style>