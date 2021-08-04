<template>
  <li>
    <label>
      <input type="checkbox" :checked="todo.done"/>
      <span>{{ todo.name }}</span>
    </label>
  </li>
</template>

<script>
export default {
  name: "Items",
  props:['todo']
}
</script>

<style scoped>

</style>